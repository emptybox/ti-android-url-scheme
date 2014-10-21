ti-android-url-scheme
=====================

Open Android app from browser (or another app) by creating a app url scheme

Using custom URL app schemes on iOS and Titanium is pretty straightforward. A few lines of code in the tiapp.xml and you’re off to the races going from app-to-browser and back or app-to-app depending on your setup. When looking for Android best practices on this….forget it. Stack Overflow? Nope. Appcelerator community Q&A? Nope. What I found were bread crumbs to keep me on the path but nothing to take me home.

Here’s what I wanted to do:

-Login via Instagram<br>
-Take user to Instagram authentication link to sign in<br>
-Once successfully authenticated, take user back to redirect uri which would open my app and pass in data with the url scheme I setup. In this case the data would come in with an intent on Android.<br>
-Parse the variables and save to device for use later on (userid, username, etc)<br>
-The trouble I was having was when I would redirect back to the app. It would either:<br>

-Not open my app and fail as a bad url in the device browser<br>
-Open my app and crash it<br>
-Or open my app and with no intent data with it (took me quite a while to get to this very exciting step)<br>
