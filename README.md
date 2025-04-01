## Reproduction steps

1. Created this project with `npx @react-native-community/cli@latest Vanilla`
2. Ran `npm install`
3. Ran `bundle install`
4. Ran `RCT_NEW_ARCH_ENABLED=0 pod install` in the `ios` folder.

There have been no changes to source files or dependencies.

## Issues

The application loads in the iOS emulator with a blank screen. No debugger can be attached.

When run from XCode, metro must be started prior, there are no error logs.

## Things I have tried 

* Removed Gemfile.lock and run `bundle install`
* Removed ios/Podfile.lock and ios/Pods and ran `bundle exec pod install`
* Run from XCode, fails to connect. Start metro then run and you get a white screen, no error logs and inability to connect debugger ("No connected targets")
* Run from `npm run ios` (even with `--client-logs`) launches with a white screen and no logs

## Specifics

Testing with IPhone 16 Pro Emulator / iOS 18.2 on a Mac Mini (2023) running Sequoia 15.3.2.