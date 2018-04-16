# Uploading Video

From your Dashboard, click on the “Media Library” icon:

![A screenshot of the dashboard, with Media Library hovered](https://eric-cloudinary-res.cloudinary.com/image/upload/q_auto,f_auto,w_900/v1518532901/Screen_Shot_2018-02-13_at_06.39.22.png)

From here, click the “more upload options” link:

![A screenshot of the Media Library with the “more upload options” link hovered](http://eric-cloudinary-res.cloudinary.com/image/upload/q_auto,f_auto,w_900/v1518534576/Screen_Shot_2018-02-13_at_06.43.29_-_with_arrow.png)

(Please note that Cloudinary is mid-flight on deploying a new Media Library UI. If you do not see a “more upload options” link, talk to Dan). 

We’re going to be grabbing our 360° video from a web address, so go ahead and paste in the following URL, and hit “upload”:

    https://res.cloudinary.com/de-demo/video/upload/v1518314168/tropical360_qjbr2d.mp4

![Screenshot of the failed upload](https://eric-cloudinary-res.cloudinary.com/image/upload/v1518534280/Screen_Shot_2018-02-13_at_06.56.33_copy.png)

What’s that? An Error? Looks like the original  four-minute HD video is a bit too big for our free-tier account. Fortunately, it’s hosted on Cloudinary, so we can just make one little change to the URL (adding `du_120`)...

    https://res.cloudinary.com/de-demo/video/upload/du_120/v1518314168/tropical360_qjbr2d.mp4

...and cut the video in half on the fly, trimming it to 120 seconds, which gets us under the limit.

![Screenshot of the successful upload](http://eric-cloudinary-res.cloudinary.com/image/upload/q_auto,f_auto,w_900/v1518534280/Screen_Shot_2018-02-13_at_06.56.33.png)

Congratulations! You’ve uploaded your first resource to Cloudinary. Now, to deliver it to a webpage...

