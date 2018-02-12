```
<!DOCTYPE html> 
<html xmlns="http://www.w3.org/1999/xhtml"> 
	<head> 
		<meta http-equiv="Content-Type" content="text/html; charset=UTF-8" /> 
		<link rel="apple-touch-icon" href="apple-touch-icon.png" />
		<title>Peter Friese's Gyro Demo</title> 
		<meta name="apple-touch-fullscreen" content="yes" />
		<meta name="apple-mobile-web-app-capable" content="yes" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no" />

		<!-- CSS  -->
		<link rel="stylesheet" type="text/css" href="https://unpkg.com/cloudinary-video-player/dist/cld-video-player.min.css">
		<link rel="stylesheet" type="text/css" href="https://rawgit.com/yanwsh/videojs-panorama/master/dist/videojs-panorama.min.css">

		<!-- JavaScript -->
		<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.2.1/jquery.min.js" type="text/javascript"></script>
		<script src="https://unpkg.com/cloudinary-core/cloudinary-core-shrinkwrap.min.js"  type="text/javascript"></script>
		<script src="https://unpkg.com/cloudinary-video-player/dist/cld-video-player.min.js" type="text/javascript"></script>
		<script src="https://rawgit.com/yanwsh/videojs-panorama/master/dist/videojs-panorama.v5.js" type="text/javascript"></script>
		<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/89/three.js" type="text/javascript" type="text/javascript"></script>
		<!-- <script src="https://unpkg.com/videojs-vr@1.0.1/dist/videojs-vr.js" type="text/javascript"></script> -->
		

		
		<style> 
		body {
			  overflow: hidden;
			  background-color: #000000;

			  user-select: none;
			  -webkit-user-select: none;
			  -moz-user-select: none;
			  -o-user-select: none;
			  -ms-user-select: none;
			}


			p {
			  color: white;
			  margin-left: 20px;
			  margin-right: 20px;
			}

		#no {
			display: none;	
		}
		
		@media screen {
			html, body, div, span {
				margin: 0;
			  padding: 0;
			  border: 0;
			  outline: 0;
			  font-size: 100%;
			  vertical-align: baseline;
			}			
			body {
				height: auto;
		  	-webkit-text-size-adjust:none;
		  	font-family:Helvetica, Arial, Verdana, sans-serif;
		  	padding:0px;
				overflow-x: hidden;		
			}		
			
			.outer {
				background: rgba(123, 256, 245, 0.9);
				padding: 0px;
				min-height: 48px;
				
			}
			
			.box {
				position: relative;
				float: left;
				width: 45%;
				padding: 7px;
				border: 1px solid rgba(255, 255, 255, 0.6);
				background: rgba(178,215,255,0.75);
				min-height: 160px;
			}	
			
			.box2 {
				position: relative;
				float: left;
				width: 45%;
				padding: 7px;
				border: 1px solid rgba(255, 255, 255, 0.6);
				background: rgba(178,215,255,0.75);
			}	
			
			.box span {
				display: block;
			}
			
			span.head {
				font-weight: bold;				
			}
		
		}
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
var canvas;
var gravity = { x: 0, y: 1 };
var delta = [ 0, 0 ];
var stage = [ window.screenX, window.screenY, window.innerWidth, window.innerHeight ];




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

 var vplayer = cld.videoPlayer("demo-player", options,onPlayerLoad).width(400)


 function onPlayerLoad(){
  // do something on player load
 } 
 
//console.log('Vplayer' , vplayer.videojs.options().plugins);
			</script> 
		</body> 
</html> 
```
