#The Cloudinary Video Player

## Here's the steps to create a simple Cloudinary video player
 
We'll use this codePen example:

<p data-height="565" data-theme-id="0" data-slug-hash="bLrwyz" data-default-tab="html,result" data-user="dzeitman" data-embed-version="2" data-pen-title="Cloudinary 360 Player - Part1" class="codepen">See the Pen <a href="https://codepen.io/dzeitman/pen/bLrwyz/">Cloudinary 360 Player</a> by Dan Zeitman (<a href="https://codepen.io/dzeitman">@dzeitman</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>


##### Include Cloudinary's JavaScript script and CSS link within your page header:

```
<head>
  ...
<script src="https://unpkg.com/cloudinary-video-player/dist/cld-video-player.min.js" type="text/javascript"></script>
<link rel="stylesheet" type="text/css" href="https://unpkg.com/cloudinary-video-player/dist/cld-video-player.min.css">
</head>
```

####HTML:
```
<!-- 
a fairly-standard HTML video element. 
Note that it does not have a src or any <source>s 
We’re going to let the Cloudinary Player create those. 
-->

<video
  id="demo-player"
  loop controls
  class="cld-video-player cld-fluid">
</video>

<!--
Any attribute that you can set on a native HTML5 player can be set on a Cloudinary player, as well. Here, I’ve used the `loop`, and `controls` attributes.

The `cld-video-player` class is mandatory, `cld-fluid` is optional, and ensures that the video is flexible/responsive-layout friendly. For 360 Player, note that the styles for the Panorama Plugin conflict with the cld-fluid class, so we'll omit them.
-->

```
####Javascript:
```
<script> 
// Cloudinary
// remember to replace cloud_name with your Cloudinary cloud name

var cld = cloudinary.Cloudinary.new({ cloud_name: "de-demo", secure: true});
 

var options = {
  publicId: 'tropical360_qjbr2d',
  crossorigin:"anonymous",
  preload:"metadata",
  loop: true,
  controls: true,
  sourceTypes: ["mp4"],
 };

 var vplayer = cld.videoPlayer("demo-player", options).width(400);

 </script> 
```
That's it.  This will create a HTML 5 Video player ready to play the tropical360_qjbr2d video.

####CodePen:
##### On CodePen they manage the header and script areas, so simply click on the setting icon and add the urls for the JavaScript and CSS directly into the settings editor:

```
https://unpkg.com/cloudinary-video-player/dist/cld-video-player.min.js
https://unpkg.com/cloudinary-video-player/dist/cld-video-player.min.css

```

