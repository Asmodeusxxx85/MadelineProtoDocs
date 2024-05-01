---
title: "messageEntityMention"
description: "Message entity mentioning a user by @username; messageEntityMentionName can also be used to mention users by their ID."
nav_exclude: true
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: messageEntityMention  
[Back to constructors index](/API_docs/constructors/index.html)



Message entity [mentioning](https://core.telegram.org/api/mentions) a user by `@username`; [messageEntityMentionName](../constructors/messageEntityMentionName.html) can also be used to mention users by their ID.

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|offset|[int](/API_docs/types/int.html) | Yes|Offset of message entity within message (in [UTF-16 code units](https://core.telegram.org/api/entities#entity-length))|
|length|[int](/API_docs/types/int.html) | Yes|Length of message entity within message (in [UTF-16 code units](https://core.telegram.org/api/entities#entity-length))|



### Type: [MessageEntity](/API_docs/types/MessageEntity.html)


### Example:

```
$messageEntityMention = ['_' => 'messageEntityMention', 'offset' => int, 'length' => int];
```  
