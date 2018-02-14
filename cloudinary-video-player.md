#The Cloudinary Video Player

## Here's the steps to create a simple Cloudinary video player
 
We'll use this codePen example:

<p data-height="565" data-theme-id="0" data-slug-hash="bLrwyz" data-default-tab="html,result" data-user="dzeitman" data-embed-version="2" data-pen-title="Cloudinary 360 Player - Part1" class="codepen">See the Pen <a href="https://codepen.io/dzeitman/pen/bLrwyz/">Cloudinary 360 Player</a> by Dan Zeitman (<a href="https://codepen.io/dzeitman">@dzeitman</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>


### Include Cloudinary's JavaScript script and CSS link within your page header:

```
		<script src="https://unpkg.com/cloudinary-video-player/dist/cld-video-player.min.js" type="text/javascript"></script>

```
### On codePen simply click on the setting icon and add the url.

```
https://unpkg.com/cloudinary-video-player/dist/cld-video-player.min.js

```

Now add the CSS:
```
<link rel="stylesheet" type="text/css" href="https://unpkg.com/cloudinary-video-player/dist/cld-video-player.min.css">

```


HTML
```
<!-- a fairly-standard HTML video element. Note that it does not have a src or any <source>s – we’re going to let the Cloudinary Player create those. -->
<video
  id="demo-player"
  loop controls
  class="cld-video-player cld-fluid">
</video>
<!--
Any attribute that you can set on a native HTML5 player can be set on a Cloudinary player, as well. Here, I’ve used the `loop`, and `controls` attributes.

The `cld-video-player` class is mandatory, `cld-fluid` is optional, and ensures that the video is flexible/responsive-layout friendly.
-->


```
