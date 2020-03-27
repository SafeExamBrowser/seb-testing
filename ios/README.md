**SEB 2.1.16 for iOS/iPadOS Preview Version**

If your are interested in testing SEB for iOS/iPadOS preview versions (using the Apple TestFlight app/service), you can send us your contact details by private message in [our discussion forum](https://sourceforge.net/p/seb/discussion/seb-ios/thread/e7e542a5/?limit=25#feaa/752c) (as GitHub doesn't support private messages) or by email to info at safeexambrowser.org.

Please give feedback through TestFlight, in our forum or by creating an issue here on our GitHub page. 

To be tested:

Version 2.1.16 adds support for hardware keyboard shortcuts to switch browser tabs and open the side menu and improves accessibility when using VoiceOver. It also includes improvements and fixes which enhance compatibility with the desktop versions of Safe Exam Browser. One issue with the new Config Key was also fixed, the Config Key can be tested by using the [prototype for an updated Moodle plugin](https://github.com/SafeExamBrowser/moodle-quizaccess_safeexambrowser) (documentation will be added soon).

As the SEB for iOS app usually is updated automatically on student devices as soon as a new version is available in the App Store, **it's important that SEB users test the beta version and report issues BEFORE the final version is released**. So if you are using SEB for iOS in your institution or distribute it with your own assessment solution, please contribute to the improvement of the SEB open source software by participating in our beta version testing. **At the same time, participating in beta testing helps you to avoid possible issues when the new version is released publicly.**


We are finally working on making SEB fully accessible, first focusing on VoiceOver compatibility.

New in build 12020:
SEBMAC-151 Listen for and block attempts to record the screen, if setting enablePrintScreen is false  (InAppSettings: Security / Allow Screen Capture).
- SEBMAC-224 Display a lock screen after a student closed their iPad case and then opened it again (iOS < 13). This is only displayed when the new setting mobileSleepModeLockScreen is true (InAppSettings: Security / Lock Screen After Sleep Mode).
Fixed issue that when locking an exam, wrong (previous) lock screen message could have been displayed.
- SEBMAC-225 Changed policy when reconfiguring with MDM settings, to prevent settings are overwritten by MDM or SEB reconfigures to client settings during a running exam, even when no plist is configured in the MDM:
1) When reconfiguring (back) to client settings
2) When opening in-app settingsS, indicating if MDM settings were received and asking if those should be applied
3) When SEB is running with client settings, there is only one browser tab (with the exam web page) open and the current URL (still) is the Start URL.
4) When secure client settings were quit and SEB is waiting to start another session.
5) When returning back to the SEB app, cases 3 or 4 apply or in-app settings are open (ask user if MDM settings should be applied)
- SEBMAC-228 Replace key string mobileShowSettings with string showSettingsInApp in default settings.
- SEBMAC-229 Fixed Browser tap setting "Show URLs: Always" in In-App-Setting (Lunch).
- SEBMAC-229 Fixed value type for "Show URLs: Always" in In-App-Setting.
- SEBMAC-234 Added error message in case AAC couldn't be started properly on older iOS versions.


New in build 11996:
- SEBMAC-227 Make UI accessible by VoiceOver: Added accessibility labels and hints to buttons and excluded unnecessary UI elements. 
- SEBMAC-227 After opening left side menu, move VoiceOver focus to the first browser tab entry.
- SEBMAC-227 Added keyboard shortcut to toggle left side menu (show/hide) Command-M for better accessibility.
- SEBMAC-227 Changed left side menu "SafeExamBrowser version number" title to a button which closes the side menu for better accessibility.
- SEBMAC-227 Activated "dynamic type" for most UI strings.

- SEBMAC-221 Again attempted to fix wrong Config Key was calculated when new default settings containing dictionaries were added in new SEB version. Removed unnecessary double calculating of new Browser Exam and Config Key after opening new config file.
- SEBMAC-225 Attempt to fix that MDM settings are not being re-applied (when settings were changed since last time applying the MDM settings or running an exam session in between) when a browser session was restarted. Attempting to fix: Settings or are overwritten by MDM, even when no plist is configured in the MDM.
- SEBMAC-199 Forwarding CustomHTTPProtocol delegate callback method sessionTaskDidCompleteSuccessfully to the webView controller as on some pages webViewDidFinishLoad was never called.
- SEBMAC-199 Replaced various error and warning log messages (which weren't actually justified there) with info and debug level.
- SEBMAC-229 Fixed setting Browser Features / "Show URLs: Always" couldn't be selected in In-App-Settings and activating this option wasn't showing the page URL in the side menu.

New in build 11947:
- SEBMAC-215 Implemented hardware keyboard shortcuts (Ctrl-Tab/Shift-Ctrl-Tab) to switch browser tabs.
- SEBMAC-212 Implemented separate settings to clear cookies when starting/ending session (keys examSessionClearCookiesOnStart / examSessionClearCookiesOnEnd). This prevents security issues with users staying logged-in after reconfiguring SEB with new settings, if this wasn't actually intended.
- SEBMAC-104 Fixed URL filter doesn't treat query strings consistently (Windows/macOS - iOS).
- SEBMAC-221 Fixed that a wrong Config Key was calculated when new default settings containing dictionaries were added in a new SEB version.
- SEBMAC-222 Fixed: Client config encrypted with password isn't compatible between Win vs. Mac+iOS.
- SEBMAC-220 Updated UI for iOS 13 build target: Fixed wrong browser toolbar (navigation bar) size/offset on iPad Pro 11/12.9" after starting SEB, enforce Light Mode, prevent dismissing in-app-settings and Initial Configuration Assistant by swiping down.
- SEBMAC-157 If checking server trust with embedded certificates, resources in subdomains of already trusted domains are now trusted as well, according to behavior in other standard browsers.