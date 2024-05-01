---
title: "messageMediaPhoto"
description: "Attached photo."
nav_exclude: true
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: messageMediaPhoto  
[Back to constructors index](/API_docs/constructors/index.html)



Attached photo.

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|spoiler|[Bool](/API_docs/types/Bool.html) | Optional|Whether this media should be hidden behind a spoiler warning|
|photo|[Photo](/API_docs/types/Photo.html) | Optional|Photo|
|ttl\_seconds|[int](/API_docs/types/int.html) | Optional|Time to live in seconds of self-destructing photo|



### Type: [MessageMedia](/API_docs/types/MessageMedia.html)


### Example:

```
$messageMediaPhoto = ['_' => 'messageMediaPhoto', 'spoiler' => Bool, 'photo' => Photo, 'ttl_seconds' => int];
```  
