<img src="https://cdn4.iconfinder.com/data/icons/logos-3/600/React.js_logo-512.png" width="100" align="left" />

# mPower React Native Port

PoC of mPower on React Native framework

## Environment Setup

[Official Docs](https://reactnative.dev/docs/environment-setup)

Homebrew :
`/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

[NodeJS](https://nodejs.org/en/)
[Flipper](https://fbflipper.com/)

Watchman:
`brew install watchman`

Yarn:
`brew install yarn`

**⚠️ Since RN 0.60+, packages are installed via `yarn`. Discard `package-lock.json` if you've accidentally run `npm install`!**

Browse to project directory and run `yarn`

#### iOS:

- Install XCode on Mac then open it for XCode Command Line Tools
- Install latest `cocoapods` gem **[ ⚠️ Make sure to match the version of Podfile, otherwise it will generate a commit and ask for pod install every time]**
  `gem install cocoapods`
- Install project pods
  `npx pod-install ios`
- open XCode with .xcworkspace file then select you Team Account, check Bundle Identifier & Provisioning Profile (if not auto)

#### Android:

- [WIP]

## Running App

**⚠️ Make sure that you add the scheme param to the end of the launch commands or select the scheme manually from XCode! The default scheme is `mPowerRN` which targets production. Example: `yarn run-ios:simulator --scheme Dev`**

You can either manually start the Metro Bundler with `yarn start` or let it automatically run after the project is built. `yarn start` command is bundled with the `--reset-cache` command.

**For ios:**

- Run on iPhone simulator (6th Gen): `yarn run-ios:phone-sim` + scheme param
- Run on connected device: `yarn run-ios:device` + scheme param

## Debugging

- if you are not using `use_frameworks!` in CocoaPods, then you can use Flipper to debug the app. When `use_frameworks!` needs to be enabled, follow the steps listed in the Podfile
- if you want to check console logs from react native code, install through :
  `brew update && brew cask install react-native-debugger`
- shake you device after you run the app and select both "Enable Live Reload" & "Start Remote JS Debugging"
