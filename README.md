# CastVideos-android

CastVideos-android application shows how to cast videos from an android device in a way that is fully compliant with the Design Checklist.

## Dependencies
* CastCompanionLibrary-android: can be downloaded here at https://github.com/googlecast/CastCompanionLibrary-android
* ShowcaseView (see change list 1.1 -> 1.2 for details)

## Setup Instructions
* Get a Chromecast device and set it up
* Register an application on the Developers Console (http://cast.google.com/publish). The easiest would be to use the Styled Media Receiver option there.
You will get an App ID when you finish registering your application.
* Setup the project dependencies
* Compile and deploy to your Android device.
* If using gradle, make sure you update build.gradle and settings.gradle to reflect the name you gave your CastCompanionLibrary project when you cloned it.
* This sample includes a published app id in the res/values/strings.xml file so the project can be built and run without a need
   to register an app id. If you want to use your own receiver, update "app_id" in that file with your own app id.

## References and How to report bugs
* [Cast Developer Documentation](http://developers.google.com/cast/)
* [Design Checklist](http://developers.google.com/cast/docs/design_checklist)
* If you find any issues with this library, please open a bug here on GitHub
* Question are answered on [StackOverflow](http://stackoverflow.com/questions/tagged/google-cast)

## How to make contributions?
Please read and follow the steps in the CONTRIBUTING.md

## License
See LICENSE

## Google+
Google Cast Developers Community on Google+ [http://goo.gl/TPLDxj](http://goo.gl/TPLDxj)

## Change List
1.3
 * Added support for Closed Captions based on enhancements made in CCL. Three new videos have been
   added to the beginning of the list of videos; these three include captions. 

1.2
 * Updated the build.gradle to work with the latest version of the Android Studio Beta (0.8.1). You may need to upgrade your
 Android Studio to be abe to work with this project.
 * Added a first-time introductory UI for the Cast Button. This is accomplished by using a [fork] (https://github.com/naddaf/ShowcaseView) of
 [ShowcaseView project] (https://github.com/amlcurran/ShowcaseView). That fork adds support for the MediaRouteButton as an ActionViewTarget.
 A pull request has also been submitted to the original project; if that gets merged in, the CastVideos project will be updated to include that dependency purely
 through the maven. Till then, that dependency is provided by inclusion of the forked library as an AAR file in the libs directory.
 If you are using Eclipse, you would need to get the forked project and include that as a library project yourself. If you decide to do so, be mindful of the
 MIN_SDK version: the forked and original projects require an API level > 10; if you need your project to run on a device with the API level 10, then
 your build may fail. To get around that, you would need to change the MIN_SDK in the forked project to 10. The included AAR library includes this change and should run on
 devices with API levels >= 10 but this feature will be hidden for level 10 and only shows up in API levels >= 11.

1.1
 * Updated the Cast button images to match the new style
 * Addressed a couple of potential leaks
