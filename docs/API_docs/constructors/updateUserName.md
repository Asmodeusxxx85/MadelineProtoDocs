---
title: "updateUserName"
description: "Changes the user's first name, last name and username."
nav_exclude: true
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: updateUserName  
[Back to constructors index](/API_docs/constructors/index.html)



Changes the user's first name, last name and username.

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|user\_id|[long](/API_docs/types/long.html) | Yes|User identifier|
|first\_name|[string](/API_docs/types/string.html) | Yes|New first name. Corresponds to the new value of **real\_first\_name** field of the [userFull](../constructors/userFull.html) constructor.|
|last\_name|[string](/API_docs/types/string.html) | Yes|New last name. Corresponds to the new value of **real\_last\_name** field of the [userFull](../constructors/userFull.html) constructor.|
|usernames|Array of [Username](/API_docs/types/Username.html) | Yes|Usernames.|



### Type: [Update](/API_docs/types/Update.html)


### Example:

```
$updateUserName = ['_' => 'updateUserName', 'user_id' => long, 'first_name' => 'string', 'last_name' => 'string', 'usernames' => [Username, Username]];
```  
