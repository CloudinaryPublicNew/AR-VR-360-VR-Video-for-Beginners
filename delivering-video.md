# Delivering Video

Your video has a public URL, which you can see in the right side of its resource details page.

![Screenshot of the details page](https://todo)

We *could* drop that URL into an HTML5 `<video>` element, and call it a day. However, for advanced uses like streaming, playlists, and you guessed it – immersive 360 video – we’re going to be using the [Cloudinary Video Player](https://TODO) to deliver our video to the web.

Here’s a CodePen showing basic Cloudinary Video Player usage. I’ve commented the relevant bits; please fork it, change the account name to your own Cloudinary account name, and work in the forked Pen for the remainder of this workshop.

<p data-height="313" data-theme-id="0" data-slug-hash="pawpVM" data-default-tab="js,result" data-user="eeeps" data-embed-version="2" data-pen-title="Cloudinary 360 Player" class="codepen">See the Pen <a href="https://codepen.io/eeeps/pen/pawpVM/">Cloudinary 360 Player</a> by Eric Portis (<a href="https://codepen.io/eeeps">@eeeps</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

As you can see, our immersive 360° video is looking pretty flat, and strange. In order to deliver an immersive video experience, we’re going to have to layer a plugin on top of the base Cloudinary Video Player. 