# Introduction
360 VR Video is becoming a popular format for creating immersive video experiences. 360 VR camera lenses capture video with wide-angle lenses and then software converts the fisheye video to equalrectangular video that looks like this:

<div style="position: relative; padding-bottom: 2%;">
{% video width="740", height="350", loop="loop", controls="controls" %}http://res.cloudinary.com/de-demo/video/upload/v1518314168/tropical360_qjbr2d.mp4{% endvideo %}
</div>

While this is interesting, it's not a fully-interactive 360° video until you play it back in a video player with 360 playback capabilities. 

Fortunately, Cloudinary's video player can easily be extended with the addition of a 360°Panorama Plugin. 

By the end of this tutorial, you will built a fully-interactive 360° video experience on the web. 

Like this:
<div style="position: relative; padding-bottom: 56.25%;">
<iframe
	src="//codepen.io/eeeps/live/MQpOpx"
	frameborder="0"
	allowfullscreen
	crossorigin="anonymous"
	style="position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
	">
</iframe>
</div>
 
Note: If video fails to appear, toggle video to full screen and back.

Cool? Right? Let’s get started.