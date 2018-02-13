# Delivering Video

Go ahead and click on the video thumbnail to get to it’s detail page.

Your video has a public URL, which you can see on the right side over here:

![Screenshot of the details page](http://eric-cloudinary-res.cloudinary.com/image/upload/f_auto,q_auto,w_900/v1518534801/Screen_Shot_2018-02-13_at_07.11.47.png)

In order to get this video onto a webpage, we *could* just drop that URL into an HTML5 `<video>` element. However, for advanced uses like adaptive streaming, playlists, and you guessed it – immersive 360 video – we’re going to supercharge the native `<video>` element with the [Cloudinary Video Player](https://demo.cloudinary.com/video-player/).

Here’s a CodePen showing basic Cloudinary Video Player usage. I’ve commented the relevant bits; please fork it, change the account name to your own Cloudinary account name, and work in the forked Pen for the remainder of this workshop.

<p data-height="313" data-theme-id="0" data-slug-hash="pawpVM" data-default-tab="js,result" data-user="eeeps" data-embed-version="2" data-pen-title="Cloudinary 360 Player" class="codepen">See the Pen <a href="https://codepen.io/eeeps/pen/pawpVM/">Cloudinary 360 Player</a> by Eric Portis (<a href="https://codepen.io/eeeps">@eeeps</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

Note that this Pen relies on loading the [Cloudinary Core JavaScript library](https://github.com/cloudinary/pkg-cloudinary-core), and the [Cloudinary Video Player JS + CSS](https://github.com/cloudinary/cloudinary-video-player). Check out the exact URLs to include in your own Pens and projects under “Settings”.

As you can see, our immersive 360° video is looking pretty flat, and strange. In order to deliver a truly immersive video experience, we’re going to have to leverage a third party plugin: [videojs-panorama](https://github.com/yanwsh/videojs-panorama).