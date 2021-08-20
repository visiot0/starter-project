# starter-project

This project is a template for initialising a new react-native project.
After having to set up the common packages I use on every project many times, I decided to make a react-native template with preinstalled packages that I use.
This template is heavy on the packages and should be checked thoroughly before usage. Also it is very opinionated when it comes to building your own folder structure as I already have the project structure included.

## Why should you use this

If you want to skip installing a ton of packages when starting a project, this might be for you.

## About the template

You can check all of the installed packages in template/package.json file, but if you want to trust my word here is what the packages inside include:

- axios
- redux
- typescript
- eslint (already setup with my custom rules)
- .env
- react-navigation v6
- splash screen
- svg
- vector icons
- react v17.0.2
- react-native v0.65.0

## Usage instructions

You can use this template with this command: `npx react-native init project-name --template https://github.com/haris523/starter-project.git`

### Android

After the installation process android app should be ready to run.
You can run the app with the following command `npx react-native run-android`

### iOS

For iOS there is an extra step. The vector icons included in the project need to be linked to file structure via xcode.
After coming to the project directory, go one step further to the ios directory and use the `pod install` command.
Open the project in xcode. Press product (8th option) at the top and then clean build folder.
After those steps you should be able to run iOS app either through xcode or with the `npx react-native run-ios` command.

## Who is this for

This project template was originally made for my team and I at visiot (https://visiot.net), to make our lives easier. 
I decided to make it public to anyone can use it. I can't promise the template will be sustained, use it at your own risk.
