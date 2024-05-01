---
title: "Secret chats"
description: "MadelineProto provides wrappers to work with secret chats."
nav_order: 25
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Secret chats

MadelineProto provides wrappers to work with secret chats.

* [Requesting secret chats](#requesting-secret-chats)
* [Accepting secret chats](#accepting-secret-chats)
* [Checking secret chat status](#checking-secret-chat-status)
* [Sending secret messages](#sending-secret-messages)

## Requesting secret chats

```php
$secret_chat = $MadelineProto->requestSecretChat($InputUser);
```

[`requestSecretChat`](https://docs.madelineproto.xyz/requestSecretChat.html) requests a secret secret chat to the [InputUser](https://docs.madelineproto.xyz/API_docs/types/InputUser.html), ID, or username specified, and returns the secret chat ID.


## Accepting secret chats

Secret chats are accepted or refused automatically, based on a value in the [settings](SETTINGS.html) (by default MadelineProto is set to accept all secret chats).

Before sending any message, you must check if the secret chat was accepted by the other client with the following method:

## Checking secret chat status

```php
$status = $MadelineProto->secretChatStatus($chat);
```

$status is `\danog\MadelineProto\MTProto::SECRET_EMPTY` if the chat cannot be found in the local database, `MTProto::SECRET_REQUESTED` if the chat was requested but not yet accepted, and `MTProto::SECRET_READY` if it is a valid accepted secret chat.

## Sending secret messages

[Full example](https://github.com/danog/MadelineProto/blob/v8/examples/secret_bot.php)

To send messages/files/service messages, simply use the sendEncrypted methods with objects that use the same layer used by the other client (specified by the number after the underscore in decryptedMessage object names, to obtain the layer that must be used for a secret chat use the following wrapper method).  

```php
$secret_chat = $MadelineProto->getSecretChat($chat);
/*
[
    'key' => [ // The authorization key
        'auth_key' => 'string', // 256 bytes long
        'fingerprint' => 10387574747492, // a 64 bit signed integer
        'visualization_orig' => 'string', // 16 bytes long
        'visualization_46' => 'string', // 20 bytes long
         // The two visualization strings must be concatenated to generate a visual fingerprint
    ],
    'admin' => false, // Am I the creator of the chat?
    'user_id' => 101374607, // The user id of the other user
    'InputEncryptedChat' => [...], // An inputEncryptedChat object that represents the current chat
    'in_seq_no_x' => number, // in_seq_no must be multiplied by two and incremented by this before being sent over the network
    'out_seq_no_x' => number, // out_seq_no must be multiplied by two and incremeneted this begore being sent over the network
    'layer' => number, // The secret chat TL layer used by the other client
    'ttl' => number, // The default time to live of messages in this chat
    'ttr' => 100, // Time left before rekeying must be done, decremented by one every time a message as encrypted/decrypted with this key
    'updated' => time(), // Last time the key of the current chat was changed
    'incoming' => [], // Incoming messages, TL serialized strings
    'outgoing' => [], // Outgoing messages, TL serialized strings
    'created' => time(), // When was this chat created
    'rekeying' => [0] // Info for rekeying
];
*/
```

This method gets info about a certain chat.

<a href="https://docs.madelineproto.xyz/docs/PROXY.html">Next section</a>