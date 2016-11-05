#This project was abandoned because [Moxie Marlinspike said he was not OK with LibreSignal using the Open Whisper Systems servers and the name "Signal"](https://github.com/LibreSignal/LibreSignal/issues/37#issuecomment-217211165).

In the same thread, Marlinspike said that he would be willing to consider ["a clean, well written, and well tested" pull request that would add WebSocket support to the Android version of Signal](https://github.com/LibreSignal/LibreSignal/issues/37#issuecomment-226646872). This would effectively eliminate Signal's dependency on GCM and thus allow the official Signal app to function on custom Android ROMs that do not include Google Play Services. There is now [a bounty on making this pull request](https://www.bountysource.com/issues/35722527-create-proper-pull-request-to-add-libresignal-s-websocket-support-to-ows-signal), and the person/team making the pull request would also receive whatever the [BitHub](https://whispersystems.org/blog/bithub/) payout would be at the time. Marlinspike expects it to have high battery consumption and an unreliable user experience, but would be fine with it if it comes with a warning and only runs in the absence of Play Services.

To be clear, Signal relying on GCM is only an issue for people who use a custom Android ROM without Google Play Services. For the vast majority of people who do have Google Play on their phone, this issue is completely irrelevant.  Signal is designed so that [GCM is only used for a wakeup event and never sees any of the encrypted Signal messages](http://support.whispersystems.org/hc/en-us/articles/215843598-Why-GCM-Does-Google-see-my-messages-).

There are two ways in which you can help make the pull request. If you are able to contribute code, check out [this page about contributing code to Signal-Android](https://github.com/WhisperSystems/Signal-Android/blob/master/CONTRIBUTING.md). If you are not able to contribute code, consider contributing to the aforementioned bounty.

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
