#This GitHub repository has been abandoned.

LibreSignal was started in February 2016 so that people using Google-free devices could communicate with people using the official Signal clients. Signal did not support these devices at the time.

The LibreSignal project never set up its own [Signal-Server](https://github.com/WhisperSystems/Signal-Server), but instead used the Open Whisper Systems servers. In May 2016, when asked if he was OK with LibreSignal using the Open Whisper Systems servers, [Moxie Marlinspike replied](https://github.com/LibreSignal/LibreSignal/issues/37#issuecomment-217211165) that he was not OK with this due to the operational costs of supporting a third-party client. A few days later, Open Whisper Systems published [their stance on federation](https://whispersystems.org/blog/the-ecosystem-is-moving/), which meant that LibreSignal users would have had to get their contacts to switch to LibreSignal if the LibreSignal project had decided to set up its own Signal-Server. However, Marlinspike [also said](https://github.com/LibreSignal/LibreSignal/issues/37#issuecomment-226646872) that he would be willing to consider "a clean, well written, and well tested" pull request that would add WebSocket support to Signal so that it could function on Google-free devices. A pull request was [eventually submitted](https://github.com/WhisperSystems/Signal-Android/pull/5962), and WebSocket support was added to Signal on [February 20, 2017](https://github.com/WhisperSystems/Signal-Android/commit/1669731329bcc32c84e33035a67a2fc22444c24b).

Signal officially supports Google-free devices as of February 20, 2017. However, before Open Whisper Systems will officially distribute Signal outside of the Google Play Store, [they would like](https://github.com/WhisperSystems/Signal-Android/commit/1669731329bcc32c84e33035a67a2fc22444c24b#commitcomment-20980219):

>1. A small well-written library that we can link into Signal which does crash reporting, checking for updates (and posting notifications for the user), and reporting basic stats.
2. A simple web-app that looks like the Play Store console, which allows us to publish new APKs, display crash reports, and display basic stats.

>Then we could link to the signed APK from our website, get crash reports and stats, and make sure users are keeping up to date.

In the meantime, you can compile Signal yourself or download the app from a third-party repository that you trust. [Here](https://github.com/WhisperSystems/Signal-Android/wiki/How-to-build-Signal-from-the-sources) is a guide for how you can download the latest Signal source code from GitHub and compile the app yourself.

Third-party repositories with rebranded versions of Signal:
* [CopperheadOS's F-droid repository](https://copperhead.co/android/docs/usage_guide#signal), which is maintained by [Daniel Micay (thestinger)](https://github.com/thestinger). The rebranded app is called Noise. Micay has said that he will continue to maintain Noise until Signal is officially distributed outside of the Google Play Store.
* The [Eutopia.cz F-droid repository](https://fdroid.eutopia.cz/), which is maintained by [Michal Krenek (xmikos)](https://github.com/xmikos). The rebranded app is called LibreSignal. Even though it is called LibreSignal, the app is not based on the code in this GitHub repository.

The following text is outdated.

# LibreSignal for Android

`LibreSignal` is the **Google-Free** fork of the original `Signal` messaging app for simple private communication with friends. `LibreSignal` uses your phone's data connection (WiFi/3G/4G) to communicate securely, optionally supports plain SMS/MMS to function as a unified messenger, and can also encrypt the stored messages on your phone. Featured on [Kuketz IT-Security Blog](https://www.kuketz-blog.de/?s=LibreSignal).

# WebSocket Support
For push notifications, Google Cloud Messaging has been completely replaced by WebSocket to directly connect to Open Whisper Systems's server.
It's done via a modified version of `libtextsecure`, which has been included as a submodule.

## Contributing Bug reports
We use GitHub for bug tracking. Please search the [existing issues](https://github.com/LibreSignal/LibreSignal/issues) for your bug and create a new one if yours is not present.

## Contributing Translations
Interested in helping to translate LibreSignal? Contribute here:

https://www.transifex.com/projects/p/signal-android/

## Contributing Code
Before contributing to LibreSignal, think about adding your code to [Signal-Android](https://github.com/WhisperSystems/Signal-Android/wiki), as we pull from there. Instructions on how to setup your development environment and build LibreSignal can be found in  [BUILDING.md](https://github.com/LibreSignal/LibreSignal/blob/master/BUILDING.md). If you're new to the LibreSignal codebase, we recommend going through our issues and picking out a simple bug to fix (check the "easy" label in our issues) in order to get yourself familiar. Also please have a look at the [CONTRIBUTING.md](https://github.com/LibreSignal/LibreSignal/blob/master/CONTRIBUTING.md), that might answer some questions.

## Contributing Ideas
Have something you want to say about LibreSignal or want to be part of the conversation? Feel invited to [post your new idea](https://github.com/LibreSignal/LibreSignal/issues/new), but please be patient for a reply and don't be mad should developers decide to not implement it or are busy with other things.

Help
====
## Support
For troubleshooting and questions, please read our [FAQ](https://github.com/LibreSignal/LibreSignal/wiki/FAQ) and see our [GitHub Issues](https://github.com/LibreSignal/LibreSignal/issues)!

## Documentation
Looking for documentation? Check out the [original Signal wiki](https://github.com/WhisperSystems/Signal-Android/wiki).

# Legal things
## Cryptography Notice

This distribution includes cryptographic software. The country in which you currently reside may have restrictions on the import, possession, use, and/or re-export to another country, of encryption software.
BEFORE using any encryption software, please check your country's laws, regulations and policies concerning the import, possession, or use, and re-export of encryption software, to see if this is permitted.
See <http://www.wassenaar.org/> for more information.

The U.S. Government Department of Commerce, Bureau of Industry and Security (BIS), has classified this software as Export Commodity Control Number (ECCN) 5D002.C.1, which includes information security software using or performing cryptographic functions with asymmetric algorithms.
The form and manner of this distribution makes it eligible for export under the License Exception ENC Technology Software Unrestricted (TSU) exception (see the BIS Export Administration Regulations, Section 740.13) for both object code and source code.

## License

Licensed under the GPLv3: http://www.gnu.org/licenses/gpl-3.0.html
