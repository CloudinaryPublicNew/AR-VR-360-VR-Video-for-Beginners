# Cloudinary Video Player

## The Cloudinary Video Player

In order to get this video onto a webpage, we _could_ just drop that URL into an HTML5 `<video>` element. However, for advanced uses like adaptive streaming, playlists, and you guessed it – immersive 360° video – we’re going to supercharge the native `<video>` element with the [Cloudinary Video Player](https://demo.cloudinary.com/video-player/).

Here’s a CodePen showing basic Cloudinary Video Player usage. I’ve commented the relevant bits; please fork it, change the account name to your own Cloudinary account name, and work in the forked Pen for the remainder of this workshop.

See the Pen [Cloudinary 360 Player](https://codepen.io/eeeps/pen/pawpVM/) by Eric Portis \([@eeeps](https://codepen.io/eeeps)\) on [CodePen](https://codepen.io).

Note that this Pen relies on loading the [Cloudinary Core JavaScript library](https://github.com/cloudinary/pkg-cloudinary-core), and the [Cloudinary Video Player JS + CSS](https://github.com/cloudinary/cloudinary-video-player). Check out the exact URLs to include in your own Pens and projects under “Settings”.

As you can see, our immersive 360° video is looking pretty flat, and strange. In order to deliver a truly immersive video experience, we’re going to have to leverage a third party plugin: [videojs-panorama](https://github.com/yanwsh/videojs-panorama).

## Code Review:

#### Include Cloudinary's JavaScript script and CSS link within your page header:

```text
<head>
  ...
<script src="https://unpkg.com/cloudinary-video-player/dist/cld-video-player.min.js" type="text/javascript"></script>
<link rel="stylesheet" type="text/css" href="https://unpkg.com/cloudinary-video-player/dist/cld-video-player.min.css">

<style>
body {
  /* center and letterbox the video */
  margin: 0;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background: black;
}

#demo-player {
  width: 100vw;
  height: calc(100vw * (9/16));
}
</style>

</head>
```

### HTML:

```text
<!-- 
a fairly-standard HTML video element. 
Note that it does not have a src or any <source>s 
We’re going to let the Cloudinary Player create those. 
-->

<video
  id="demo-player"
  loop controls
  class="cld-video-player">
</video>

<!--
Any attribute that you can set on a native HTML5 player can be set on a Cloudinary player, as well. Here, I’ve used the `loop`, and `controls` attributes.

The `cld-video-player` class is mandatory.
-->
```

### Javascript:

#### Minimal Code

```text
/* create and initalize a Cloudinary instance */
var cld = cloudinary.Cloudinary.new({
  cloud_name: "de-demo", /* 👈 change this to your cloud name! */
  secure: true /* use https everywhere */
});

var options = {
  publicId: "tropical360_qjbr2d", /* the video public ID. Yours should be the smae */
  sourceTypes: ["mp4"]
};

/* take our <video> element and give it Cloudinary Video Player superpowers */

var vplayer = cld.videoPlayer(document.getElementById("demo-player"), options);
```

#### Additional code to add player controls and deal with cross origin hosted media.

```text
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

That's it. This will create a HTML 5 Video player ready to play the tropical360\_qjbr2d video.

### CodePen:

#### On CodePen they manage the header and script areas, so simply click on the setting icon and add the urls for the JavaScript and CSS directly into the settings editor:

```text
https://unpkg.com/cloudinary-video-player/dist/cld-video-player.min.js
https://unpkg.com/cloudinary-video-player/dist/cld-video-player.min.css
```

