# REACT NATIVE starter-project

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
- react-native v0.65.1

## Usage instructions

You can use this template with this command: `npx react-native init project-name --template https://github.com/haris523/starter-project.git`

Use `npx react-native-rename "Travel App" -b com.junedomingo.travelapp` command in your project and change the `"Travel App"` name to your project name and the
`com.junedomingo.travelapp` package to what you want it to be (com.yourappname).
After that use `pod install` from your iOS folder and run `watchman watch-del-all` from your project folder and also run `npm start --reset-cache`

Also be sure to remove package-lock.json. Optionally also change Starter project on LaunchScreen.storyboard to something else.

### Android

After the installation process android app should be ready to run.
You can run the app with the following command `npx react-native run-android`

### iOS

For iOS there is an extra step. The vector icons included in the project need to be linked to file structure via xcode.
After coming to the project directory, go one step further to the ios directory and use the `pod install` command.
Open the project in xcode. Press product (8th option) at the top and then clean build folder.
After those steps you should be able to run iOS app either through xcode or with the `npx react-native run-ios` command.

## Additional info

I'll write here about the additional configurations the user needs/should do to get the best possible experience from the template.

### Themes

App.js has been wrapped by ThemeProvider, which can have an initial value (this is mainly used to persist theme between closing and opening the app, and saving the theme under some key in async storage).

#### Required steps for setting up themes

Firstly you want to put all of your themes inside the themes object, and for each theme define the attributes with your theme configuration. Head to `./src/theme/themes.ts` file and set up your themes as it was given in the template. Follow the instructions in the comments.

To actually use those themes, import useTheme hook from the hooks folder. useTheme hook returns theme, themeName, and setTheme function. An example of this can be found inside `./src/screens/Home` folder.

## Who is this for

This project template was originally made for my team and I at visiot (https://visiot.net), to make our lives easier.
I decided to make it public to anyone can use it. I can't promise the template will be sustained, use it at your own risk.
