# VideoJs-Panorama Plugin

The plugin we’re going to be using is called [videojs-panorama](https://github.com/yanwsh/videojs-panorama).

Incidentally – this is not a plugin made specifically for Cloudinary’s player. But Cloudinary built its player on top of the widely used [VideoJS](http://videojs.com) framework, and plugins for VideoJS work on the Cloudinary Player, as well.

**INSTALL PLUGIN:**

## Replace the Cloudinary options with one containing the plugin object configured for the panorama plugin:

```text
var options = {
  publicId: "tropical360_qjbr2d",
  plugins: {
    panorama: {
      clickAndDrag: true,
      clickToToggle: true,
      autoMobileOrientation: true
    }
  },
  sourceTypes: ["mp4"]
};
```

See the Pen [Cloudinary 360 Player](https://codepen.io/eeeps/pen/MQpOpx/) by Eric Portis \([@eeeps](https://codepen.io/eeeps)\) on [CodePen](https://codepen.io).

