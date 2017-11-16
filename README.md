# Kitchensink/Boilerplate for Cordova-PhoneGap-Babel-React-Hotloader-Webpack-Framework7-Firestore-FontAwesome
Template for ready-to-use hybrid mobile apps with native look.

## Preview
![Material](https://raw.github.com/vonubisch/Cordova-PhoneGap-Babel-React-Hotloader-Webpack-Framework7-Firestore-FontAwesome/master/res/demo/preview-android.png)

## Tools
Not all are correctly implemented/configured yet.
- Apache Cordova - *to compile to iOS and Android Apps*
- Adobe PhoneGap - *some juicy Cordova tools*
- React - *DOM ninja*
- React Hotloading - *No more F5*
- Babel - *for sexy JS*
- Firestore - *store files and data*
- Webpack - *Pack it up*
- ESlint - *only pretty code*
- Framework7 - *CSS framework native iOS/Android*
- FontAwesome - *good old icons*

## This repo is kinda ready for use
Things to do:
- Demo Firestore
- Demo more UI stuff with Framework7
- Cleanup node_modules
- Figure out if actually builds to an app

## Firestore config
    const firebaseConfig = {
        apiKey: "xxx",
        authDomain: "xxx.firebaseapp.com",
        databaseURL: "https://xxx.firebaseio.com",
        projectId: "xxx",
        storageBucket: "xxx.appspot.com",
        messagingSenderId: ""
    };

## Start application
Run via the CLI:
```
git clone git@github.com:vonubisch/Cordova-PhoneGap-Babel-React-Hotloader-Webpack-Framework7-Firestore-FontAwesome.git my-app
npm install
npm run start
```
Then open the browser at:
```
http://localhost:8080
```

## Build the app for production
Make sure Cordova has its platforms
```
cordova platform add android
cordova platform add ios
cordova platform add browser
```
To build the app without the hotreloader:
```
npm run build [ -- ios || android]
npm run prepare -- ios
npm run prepare -- android
```
This will switch your config.xml file to production mode, build the app bundle to `www` using Webpack and run `cordova build` for you.

Then you can run Cordova / PhoneGap like `phonegap serve` or `cordova run ios`

Now you can use the PhoneGap developer app or browser to view your app.
