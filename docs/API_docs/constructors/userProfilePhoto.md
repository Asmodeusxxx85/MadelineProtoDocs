---
title: "userProfilePhoto"
description: "User profile photo."
nav_exclude: true
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: userProfilePhoto  
[Back to constructors index](/API_docs/constructors/index.html)



User profile photo.

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|has\_video|[Bool](/API_docs/types/Bool.html) | Optional|Whether an [animated profile picture](https://core.telegram.org/api/files#animated-profile-pictures) is available for this user|
|personal|[Bool](/API_docs/types/Bool.html) | Optional|Whether this profile photo is only visible to us (i.e. it was set using [photos.uploadContactProfilePhoto](../methods/photos.uploadContactProfilePhoto.html)).|
|photo\_id|[long](/API_docs/types/long.html) | Yes|Identifier of the respective photo|
|stripped\_thumb|[bytes](/API_docs/types/bytes.html) | Optional|[Stripped thumbnail](https://core.telegram.org/api/files#stripped-thumbnails)|
|dc\_id|[int](/API_docs/types/int.html) | Yes|DC ID where the photo is stored|



### Type: [UserProfilePhoto](/API_docs/types/UserProfilePhoto.html)


### Example:

```
$userProfilePhoto = ['_' => 'userProfilePhoto', 'has_video' => Bool, 'personal' => Bool, 'photo_id' => long, 'stripped_thumb' => 'bytes', 'dc_id' => int];
```  
