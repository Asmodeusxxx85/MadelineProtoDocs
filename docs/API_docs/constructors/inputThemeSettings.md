---
title: "inputThemeSettings"
description: "Theme settings"
nav_exclude: true
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: inputThemeSettings  
[Back to constructors index](/API_docs/constructors/index.html)



Theme settings

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|message\_colors\_animated|[Bool](/API_docs/types/Bool.html) | Optional|If set, the freeform gradient fill needs to be animated on every sent message|
|base\_theme|[BaseTheme](/API_docs/types/BaseTheme.html) | Yes|Default theme on which this theme is based|
|accent\_color|[int](/API_docs/types/int.html) | Yes|Accent color, ARGB format|
|outbox\_accent\_color|[int](/API_docs/types/int.html) | Optional|Accent color of outgoing messages in ARGB format|
|message\_colors|Array of [int](/API_docs/types/int.html) | Optional|The fill to be used as a background for outgoing messages, in RGB24 format. <br>If just one or two equal colors are provided, describes a solid fill of a background. <br>If two different colors are provided, describes the top and bottom colors of a 0-degree gradient.<br>If three or four colors are provided, describes a freeform gradient fill of a background.|
|wallpaper|[InputWallPaper](/API_docs/types/InputWallPaper.html) | Optional|[inputWallPaper](../constructors/inputWallPaper.html) or [inputWallPaperSlug](../constructors/inputWallPaper.html) when passing wallpaper files for [image](https://core.telegram.org/api/wallpapers#image-wallpapers) or [pattern](https://core.telegram.org/api/wallpapers#pattern-wallpapers) wallpapers, [inputWallPaperNoFile](../constructors/inputWallPaperNoFile.html) with `id=0` otherwise.|
|wallpaper\_settings|[WallPaperSettings](/API_docs/types/WallPaperSettings.html) | Optional|[Wallpaper](https://core.telegram.org/api/wallpapers) settings.|



### Type: [InputThemeSettings](/API_docs/types/InputThemeSettings.html)


### Example:

```
$inputThemeSettings = ['_' => 'inputThemeSettings', 'message_colors_animated' => Bool, 'base_theme' => BaseTheme, 'accent_color' => int, 'outbox_accent_color' => int, 'message_colors' => [int, int], 'wallpaper' => InputWallPaper, 'wallpaper_settings' => WallPaperSettings];
```  
