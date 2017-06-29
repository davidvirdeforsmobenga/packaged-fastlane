# packaged-fastlane 🚀

## Prerequisites
- Ruby 2.1.0 or later.
- aws-sdk-v1 `gem install aws-sdk-v1`
- rake `gem install rake`

## Create the package 🛠
Run `rake package:standalone:zip` to compile and build a package containing both ruby and `fastlane`. 

This job queries RubyGems to get the most recent version that is available and builds that version of `fastlane`. By running `rake --tasks` you should also be able to predict what version will be built as that will also make the call to fetch the most recent version from RubyGems.

### Cleanup 🚿
Run tasks in the `package:clean` namespace to clean up after yourself if you'd like.

## Using the package 📦
In a terminal, call `path/to/bundle-x.x.x/fastlane` followed by a normal call to any `fastlane` action, lane, or tool (i.e. snapshot, gym, etc.).

## Background 🍫
The heavy lifting of this project is handled by work done by the [CocoaPods team](https://cocoapods.org/about#team) for the [CocoaPods-app](https://github.com/CocoaPods/CocoaPods-app). They deserve many thanks for helping to make _packaged fastlane_ possible!
