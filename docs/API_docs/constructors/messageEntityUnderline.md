---
title: "messageEntityUnderline"
description: "Message entity representing underlined text."
nav_exclude: true
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: messageEntityUnderline  
[Back to constructors index](/API_docs/constructors/index.html)



Message entity representing underlined text.

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|offset|[int](/API_docs/types/int.html) | Yes|Offset of message entity within message (in [UTF-16 code units](https://core.telegram.org/api/entities#entity-length))|
|length|[int](/API_docs/types/int.html) | Yes|Length of message entity within message (in [UTF-16 code units](https://core.telegram.org/api/entities#entity-length))|



### Type: [MessageEntity](/API_docs/types/MessageEntity.html)


### Example:

```
$messageEntityUnderline = ['_' => 'messageEntityUnderline', 'offset' => int, 'length' => int];
```  
