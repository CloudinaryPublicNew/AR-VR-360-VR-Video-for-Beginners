# Add C\# Script & Watson Credentials

I did most of the hard work for you. Is it production worthy code? I mean, probably not. Does it get you inspired to write production code? Of course!

[**akeller/Unity-AI-AR**  
_Contribute to Unity-AI-AR development by creating an account on GitHub._github.com](https://github.com/akeller/Unity-AI-AR)



The repo linked above contains a single C\# file you can copy over. I recommend opening it \(or copying it into\) your favorite IDE or text editor and make the changes below.

If you need step-by-step instructions for creating the Watson Services, checkout the[README](https://github.com/akeller/Unity-AI-AR/blob/master/README.md)before proceeding.

Make sure to add your credentials as strings \(double quotes\). Unless you made changes to the file already, here’s the line numbers \(or approximate line numbers\):

* Line 27: Add your Conversation workspace id.
* Line 264: Add your Conversation username and password as a string.
* Line 269: Add your Text-to-Speech username and password as a string.
* Line 274: Add your Speech-to-Text username and password as a string.

In Unity under hierarchy, click your CyberSolider \(remember its a child of ImageTarget which may be collapsed\). In the Inspector click the “Add Component” button and scroll to the bottom of the list for “New Script”. Call it “SoldierConvo” unless you want to call it something different in which case you will need to update the C\# code. Make sure the language is C sharp and hit the “Create and add” button. This will attach a new C\# file to your CyberSoldier GameObject and give it the ability to speak and listen.

Copy and paste the C\# code from your text editor or IDE. If you named the file something different, make sure the code reflects that.

At this point, you should be able to save and build your C\# file. Make sure there are no errors.

If the build is successful, you should now be able to hit the play button on your Unity Editor and hear Watson! Look for output in the console too. Speak back and notice Watson is listening too.

![](https://cdn-images-1.medium.com/max/1600/1*5ajdgIkzjlQC4d_0ESBrNA.png)

That time I ordered a “she’s” pizza

Feel free to stop here and do a little searching to steps to deploy to Android. Or deploy nowhere and happily run it on your laptop! Up to you.

  


