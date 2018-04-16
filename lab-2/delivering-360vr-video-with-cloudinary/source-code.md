# Source Code

```text
<!DOCTYPE html> 
<html xmlns="http://www.w3.org/1999/xhtml"> 
    <head> 
        <meta http-equiv="Content-Type" content="text/html; charset=UTF-8" /> 
        <link rel="apple-touch-icon" href="apple-touch-icon.png" />
        <title>Cloudinary 360VR Video Demo</title> 
        <meta name="apple-touch-fullscreen" content="yes" />
        <meta name="apple-mobile-web-app-capable" content="yes" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no" />

        <!-- CSS  -->
        <link rel="stylesheet" type="text/css" href="https://unpkg.com/cloudinary-video-player/dist/cld-video-player.min.css">
        <link rel="stylesheet" type="text/css" href="https://rawgit.com/yanwsh/videojs-panorama/master/dist/videojs-panorama.min.css">

        <!-- JavaScript -->
        <script src="https://unpkg.com/cloudinary-core/cloudinary-core-shrinkwrap.min.js"  type="text/javascript"></script>
        <script src="https://unpkg.com/cloudinary-video-player/dist/cld-video-player.min.js" type="text/javascript"></script>
        <script src="https://rawgit.com/yanwsh/videojs-panorama/master/dist/videojs-panorama.v5.js" type="text/javascript"></script>
        <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/89/three.js" type="text/javascript" type="text/javascript"></script>




        <style> 

        </style> 
    </head> 

    <body>
    <video
    crossorigin="anonymous"
    id="demo-player"
    controls
    autoplay
    class="cld-video-player">
    </video>

<script> 

// Cloudinary

var cld = cloudinary.Cloudinary.new({ cloud_name: "de-demo", secure: true});


var options = {
   publicId: 'tropical360_qjbr2d',
    plugins: {

    panorama: {
      PanoramaThumbnail: true, //enable panorama thumbnail
      KeyboardControl: true,
      clickAndDrag: true,
      clickToToggle: true,
      autoMobileOrientation: true,
      videoType: 'equirectangular', //'fisheye','equirectangular',
    }
  },
  crossorigin:"anonymous",
  preload:"metadata",
  loop: true,
  controls: true,
  autoplayMode: 'on-scroll',
  transformation: [{ width: 800  }, {}],
  sourceTypes: ["mp4"],
 };

 var vplayer = cld.videoPlayer("demo-player", options).width(400)

</script> 
</body> 
</html>
```

