**SEB 2.1.16 for iOS/iPadOS Preview Version**

If your are interested in testing SEB for iOS/iPadOS preview versions (using the Apple TestFlight app/service), you can send us your contact details by private message in [our discussion forum](https://sourceforge.net/p/seb/discussion/seb-ios/thread/e7e542a5/?limit=25#feaa/752c) (as GitHub doesn't support private messages) or by email to info at safeexambrowser.org.

Please give feedback through TestFlight, in our forum or by creating an issue here on our GitHub page. 

To be tested:

Version 2.1.16 adds support for hardware keyboard shortcuts to switch browser tabs, improvements and fixes which enhance the compatibility with the desktop versions of Safe Exam Browser. One issue with the new Config Key was also fixed, the Config Key can be tested by using the [prototype for an updated Moodle plugin](https://github.com/SafeExamBrowser/moodle-quizaccess_safeexambrowser) (documentation will be added soon).

As the SEB for iOS app usually is updated automatically on student devices as soon as a new version is available in the App Store, **it's important that SEB users test the beta version and report issues BEFORE the final version is released**. So if you are using SEB for iOS in your institution or distribute it with your own assessment solution, please contribute to the improvement of the SEB open source software by participating in our beta version testing. **At the same time, participating in beta testing helps you to avoid possible issues when the new version is released publicly.**


New in build 11947:
- SEBMAC-215 Implemented hardware keyboard shortcuts (Ctrl-Tab/Shift-Ctrl-Tab) to switch browser tabs.
- SEBMAC-212 Implemented separate settings to clear cookies when starting/ending session (keys examSessionClearCookiesOnStart / examSessionClearCookiesOnEnd). This prevents security issues with users staying logged-in after reconfiguring SEB with new settings, if this wasn't actually intended.
- SEBMAC-104 Fixed URL filter doesn't treat query strings consistently (Windows/macOS - iOS).
- SEBMAC-221 Fixed that a wrong Config Key was calculated when new default settings containing dictionaries were added in a new SEB version.
- SEBMAC-222 Fixed: Client config encrypted with password isn't compatible between Win vs. Mac+iOS.
- SEBMAC-220 Updated UI for iOS 13 build target: Fixed wrong browser toolbar (navigation bar) size/offset on iPad Pro 11/12.9" after starting SEB, enforce Light Mode, prevent dismissing in-app-settings and Initial Configuration Assistant by swiping down.
- SEBMAC-157 If checking server trust with embedded certificates, resources in subdomains of already trusted domains are now trusted as well, according to behavior in other standard browsers.
