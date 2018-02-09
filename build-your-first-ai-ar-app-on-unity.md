# Build Your First AI AR App on Unity {#a5e6}

#### [Amara Keller](https://medium.com/@MissAmaraKay?source=user_popover)

###### [Medium Jan 4, 2018](https://medium.com/@MissAmaraKay/build-your-first-ai-ar-app-on-unity-8c12895687fa)

## Then Deploy to iOS So You Can Impress Your Friends {#6658}

I’ve been busy trying to make a demo that incorporates Watson API Services on Unity for workshops in early 2018. Naturally most of my time has been sunk into making it as overly complicated for myself as possible.

Here’s my exact thought process, spread across about 4 working days:

> I need to refresh my C\# skills and learn the Unity Editor. I want to build an AR app in Unity. Are there any plugins or packages I can use? Yes! Vuforia looks interesting let me do something with ImageTargets and see if I can play with some free assets. I’ll use Watson Conversation, but also Watson Speech-to-Text and Text-to-Speech, and the Conversation Slots Code Pattern because its prebuilt and I like pizza. Then I’m going to deploy it to my iPhone, mostly so I can run around and talk to Watson in real life, but also so I can eventually use Smart Terrain and put whatever asset I’m using to help me build my pizza literally everywhere. Now how do I attach a script to a GameObject?

That’s a literal window into my brain, and often why I say I cant come up with a creative demo idea because I get too busy making it huge. Why didn’t I just stop at any point? Doesn’t matter now, let’s dive into it.

### Some Assumptions/Pre-requisites {#af75}

* I’m running a MacBook Pro and an iPhone on iOS9+ so that’s going to be how this is written.
* You will need an
  [**IBM Cloud account**](http://bluemix.net/)
  and credentials for
  **Watson Conversation, Speech-to-Text, and Text-to-Speech**
  . Step-by-step instructions
  [available](https://github.com/akeller/Unity-AI-AR/blob/master/README.md)
  .
* **Download Unity, check box for iOS Build Support and Vuforia Augmented Reality Support**
  . I’m running 2017.3.Of3 Personal, the free version, on High Sierra. I started this app on 2017.2.Of3 and converted it over which wasn’t terrible, but because I pulled in a bunch of free assets to play around with it took some time to reimport them.
* **Download Xcode.**
  You won’t need it immediately \(Unity will download with MonoDevelop\) but you will need it to deploy your app.



