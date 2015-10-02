---
layout: v2_fluid/docs_base
category: platform
id: camera
title: Ionic 2 Plugins | Camera
header_title: Camera - Ionic 2 Plugins
header_sub_title: Ionic 2 Developer Preview
---
<div class="improve-docs">
  <a href='https://github.com/driftyco/ionic-site/edit/ionic2/docs/v2/plugins/camera/index.md'>
    Improve this doc
  </a>
</div>

<h1 class="title">Camera</h1>

To take pictures in your Ionic app, use the `Camera` utility from ngCordova:

```javascript
import {Camera} from 'ngcordova'

class PhotoTaker {
  constructor() {
  }

  takePhoto() {
    Camera.getPicture({
      quality: 50,
      destinationType: Camera.DestinationType.DATA_URL,
      sourceType: Camera.PictureSourceType.CAMERA,
      allowEdit: true,
      encodingType: Camera.EncodingType.JPEG,
      targetWidth: 100,
      targetHeight: 100,
      popoverOptions: CameraPopoverOptions,
      saveToPhotoAlbum: false
    }).then((data) => {
      // Camera data
    })
  }
}
```