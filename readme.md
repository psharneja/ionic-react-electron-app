# Ionic - Android, ios, electron

## To create a new app
1. install ionic cli using `npm install -g @ionic/cli`
2. ionic start, choose the type of app (js, angular, ios, vue) or
```ionic start ionic-react-electron-app tabs --type=react --capacitor```
3. startup steps to start with a new react app: [here](https://ionicframework.com/docs/react/your-first-app
) 
4. you need below toolings. (cordova-res for copying icons and splash screens, check [here](https://ionicframework.com/docs/cli/commands/cordova-resources))
```npm install -g native-run cordova-res```
5. run using `npm run start`
5. build steps are as mentioned for this app.

This Ionic app supports android, ios and electron build. electron build can be used to create windows or mac setup files (exe or dmg). clone this repo and......

## Installation

Use the package manager npm to install.

```bash
npm install
```

## build
```
ionic build
```

### add different builds
 1. android 
```
npx cap add android
```
2. ios
```
npx cap add ios
```
3. electron
```
npx cap add @capacitor-community/electron
```

## Sync your build code with live code
```
npx cap sync
```

## Android build
1. ionic build
2. npx cap add android (if not added already, else skip)
3. npx cap sync (only if you did any code change after adding the platform)
4. npx cap open android (opens build in android studio, you need android studio and gradle installed)
5. build an apk like any other android native code. Tools -> build apk / build signed apk

## ios build
1. ionic build
2. npx cap add ios (if not added already, else skip)
3. npx cap sync (only if you did any code change after adding the platform)
4. npx cap open ios (opens build in code, u need xcode tools installed)
5. create your ios build like any native ios app.


## electron build
1. ionic build
2. npx cap add @capacitor-community/electron (if not added already, else skip)
3. npx cap sync (only if you did any code change after adding the platform)
4. if you don't want to create an executable and just look at how your electron app works: ```npx cap open @capacitor-community/electron```
5. open electron directory created with previous step.
```cd electron```
6. inside electron directory, create windows build ``` npm run electron:build-windows ```
7. inside electron directory, create mac build ``` npm run electron:build-mac ```
