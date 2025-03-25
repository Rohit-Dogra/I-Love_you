# i love you :heart:
making long distance a little easier
![Screenshot 2025-03-25 100601](https://github.com/user-attachments/assets/7805e40f-5eed-4485-b701-3eb61bcec817)

# why?

I made this for my girlfriend. She lives in another city, I live in the Patiala . Also, because!

Tap the heart on the page, and a ripple is transmitted to everybody else on that page. When they respond, you see their ripple too.



![i love you]



You can test it out here. Thanks to the Red Hat Openshift free tier, the nodejs part of this app is hosted online!
Try out a private room

# installation

    npm install
    port=8123 npm run start

Note the `port` variable. Set this to whatever you like.

Then, at the bottom of `./site/index.html` adjust the port number & remove/modify the Google Analytics snippet.

Do the same thing at the bottom of `./site/main.js`.

... Then direct your web server at the `./site` directory and have fun!

NB: The front end is not served through the corresponding nodejs application in this repo.

# releasing
In `Gruntfile.js` edit the `s3:{}` task to specify your AWS bucket region & name. You can also hardcode key and secret here but be careful with public repos.

Then, run this in your CLI:

    key=XXXXXX secret=XXXXXX npm run deploy

You can also make a `.env` file and store the variables in there. The file is ignored by git, so you don't have to fear pushing up keys.
