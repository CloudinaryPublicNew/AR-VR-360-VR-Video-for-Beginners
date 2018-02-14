# The `videojs-panorama` plugin

The plugin we’re going to be using is called [videojs-panorama](https://github.com/yanwsh/videojs-panorama).

Incidentally – this is not a plugin made specifically for Cloudinary’s player. But Cloudinary built its player on top of the widely used [VideoJS](http://videojs.com) framework, and plugins for VideoJS work on the Cloudinary Player, as well.


**INSTALL PLUGIN:**

#### Replace the Cloudinary options with one containing the plugin object configured for the panorama plugin:
```
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

<p data-height="565" data-theme-id="0" data-slug-hash="MQpOpx" data-default-tab="result" data-user="eeeps" data-embed-version="2" data-pen-title="Cloudinary 360 Player" data-editable="true" class="codepen">See the Pen <a href="https://codepen.io/eeeps/pen/MQpOpx/">Cloudinary 360 Player</a> by Eric Portis (<a href="https://codepen.io/eeeps">@eeeps</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>