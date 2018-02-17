# Configure Vuforia Image Database \(ImageTarget\)

_Disclaimer:_In this section,_y_ou are going to be working in the Unity Editor and a browser, flipping back and forth between the two. I think this makes the most sense for learning, even if it feels a little annoying.

Head over the[Vuforia Developer Portal](https://developer.vuforia.com/). Create an account if you haven’t already and log in. You should see the License Manager after you login. Click “Get Development Key” and name it something interesting \(perhaps the same interesting thing you named your app!\)

Click your license in the License Manager and copy your license key.

Go back to the Unity Editor and add an ARCamera. Click Create \(just underneath Hierarchy\) or go to GameObject &gt; Vuforia. Select ARCamera and watch it appear on your Hierarchy. \(Feel free to delete your Main Camera now.\) Click the ARCamera and open the inspector. Find the Vuforia Behaviour \(Script\) section and click the button “Open Vuforia configuration”.

Paste your license key into the “App License Key” input.

Go back to your Vuforia Developer Portal and click Target Manager. Click the “Add Database” button. As usual, name your database something interesting and select “Device” for the type. Click Create.

![](https://cdn-images-1.medium.com/max/1600/1*SMFA4S9bSGaPPPCyC5eZTQ.png)

Click on the name of your new database. This allows your to add images to project your Cyber Soldier onto. These are called “[TargetImages](https://library.vuforia.com/articles/Training/Image-Target-Guide.html)” and they need to be highly random \(no patterns\). Vuforia has a number of examples using rocks, so I went ahead and stuck with the rocks. Get the rocks by a quick Google search for “Vuforia stones”.

Download your stones or rocks \(what’s the difference, really?\). Print it \(B&W or color, doesn’t matter\). Click “Add Target”. We are adding a Target of type Single Image. Choose your rocks in the file chooser, give it a width of 50, and make sure the name is unique but not so unique you forget what it is. Click Add.

![](https://cdn-images-1.medium.com/max/1600/1*_c_PGlp8j96_0Dj1rUb31g.png)

Vuforia will do some processing so you’ll see the status flip to Active when its done. Your star rating depends on the randomness of your image and how good a TargetImage it is. Notice the rocks gives a 5 star rating. I took a picture of the fake wood grain of my office desk and it got a solid 0 star rating.

![](https://cdn-images-1.medium.com/max/1600/1*ALJ8zNH9e4kR7WOdpajbsA.png)

Click “Download Database \(All\).

Go back to your Unity Editor \(isn’t this flipping back and forth fun?!\) and while still in your Vuforia Configuration find the section for Databases and check the boxes to load and activate your database.

Create an ImageTarget by clicking GameObject &gt; Vuforia &gt; Image. In the Image Target Behaviour \(Script\), make sure the database is set to the one you just created and the Image Target is set to your stones.

Move your CyberSolider into the ImageTarget so it becomes a child of that GameObject.

![](https://cdn-images-1.medium.com/max/1600/1*8Jh3zuIdBzNOwX4MBDsSzg.png)

You should now see your Cyber Soldier standing on some rocks. You could be an overachiever like me and your Cyber Soldier is also holding a pizza slice. Because, why not?

![](https://cdn-images-1.medium.com/max/1600/1*7Mo5ZGNaiX6BLgWwLd7wbQ.png)

Pizza sliced wedged into my Cyber Soldier’s hand \(pizza requires additional assets\).

As a future item, I’d like to convert this to using Smart Terrain or Ground Planes instead of ImageTargets. As fun as ImageTargets are, I think they might limit inspiration of other interesting ways to use VR.

  


