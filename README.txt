RECTOR COUGARS APP - how to get it on Google Play
==================================================

STEP 1: Put the app online (free)
  1. Make a free account at github.com
  2. Create a new repository named:  rector-cougars
  3. Upload every file in this folder (index.html, manifest.json, sw.js, the .png icons)
  4. In the repo: Settings > Pages > Source: "Deploy from a branch" > Branch: main > Save
  5. After a minute your app is live at:
        https://YOUR-USERNAME.github.io/rector-cougars/
     Open it on a phone to test.

STEP 2: Turn it into an Android package (free)
  1. Go to pwabuilder.com
  2. Paste your URL from Step 1 and click Start
  3. Click "Package for stores" > Android > Generate
  4. Download the zip. Inside is an .aab file (the app) and a signing key.
     KEEP THE SIGNING KEY FILE SAFE - you need the same key for every future update.

STEP 3: Publish (needs an adult with a Google account, $25 one time)
  1. play.google.com/console > create developer account
  2. Create app > name "Rector Cougars" > Free > App
  3. Fill in the store listing (description, screenshots from your phone, the icon-512.png)
  4. Testing > Closed testing > upload the .aab > add 12+ testers by email
  5. After 14 days of testing, apply for production access, then release.

Updating the app later: edit index.html, re-upload to GitHub, regenerate in PWABuilder,
upload the new .aab to Play Console.
