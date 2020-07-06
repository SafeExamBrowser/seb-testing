**SEB 2.1.5 for macOS Preview Version**

Here you can find the current preview build of the next release of SEB for macOS. A preview version doesn't contain the full functionality of the final release yet, but specific new features and fixes for issues of the current stable release. 

You can support us by testing the pre-release version and give feedback in our forum or by creating an issue here on our GitHub page. 


New in SEB 2.1.5pre3 for macOS (2BD3):
- SEBMAC-246 Added support for Web Inspector, key allowDeveloperConsole = true (default false), setting in Browser pane / "Enable Web Inspector (developer tools)".
Right click has to be enabled (see Security/Hooked Keys/Enable Right Mouse) to access the context menu on web page elements.
- Removed setting for disabling Local Storage (in Browser pane). Local Storage is now always enabled.
- SEBMAC-238 Fixed: Browser Exam and Config Key are not displayed and Settings flagged as changed.
- SEBMAC-232 Fixed: SEB crashes when switching between Preferences panes.
- SEBMAC-231 Added all SEB for iOS settings in Preferences / Exams pane. Rearranged UI in Exam preferences pane further and embedded the whole pane content into a scroll view. Added settings for clear session cookies on start/end to Exam pane.
- Changed log level for adding certificates from Keychain from Debug to Verbose.


New in SEB 2.1.5pre2 for macOS (2BD3):
- SEBMAC-212 Implemented setting keys to clear cookies when starting/ending session. This prevents security issues with users staying logged-in after reconfiguring SEB with new settings, if this wasn't actually intended. The setting keys examSessionClearCookiesOnStart / examSessionClearCookiesOnEnd are supported, but cannot yet be set in SEB's preferences window in this build, but you can use settings generated in the current iOS 2.1.16 beta build.
- SEBMAC-221 Definitely fixed that a wrong Config Key was calculated, when new default settings containing dictionaries were added in new SEB version.
- Fixed an issue in previous preview build: Imported config not containing all setting key/values had wrong default values for the missing keys added.
- SEBMAC-230 SEB Fixed config without proper MIME type isn't recognized: Added "text/xml" as alternative MIME type for SEB Config Files when a seb(s) link is opened.
- SEBMAC-221 Merged seb-ios into master, ongoing work for common codebase for macOS and iOS version 2.2.


New in SEB 2.1.5pre1 for macOS (2B82):

- SEBMAC-221 Fixed: Wrong Config Key is calculated when new SEB version adds new default settings which is a dictionary/array.
- SEBMAC-223 Removed ARDAgent from detecting Remote Management:
ARDAgent is running always when Remote Management is enabled in System Preferences / Sharing. It should be enough to detect the processes ScreensharingAgent and AppleVNCServer (Back to My Mac on macOS < 10.14 Mojave).
- SEBMAC-222 Fixed: Client config encrypted with password isn't compatible between Win vs. Mac+iOS.
Problem with uppercase/lowercase password hashes, solved by encrypting with lowercase hash (like in Windows version) and decrypting by both lowercase (for client config saved in Win and macOS 2.1.15+ version) and lowercase (macOS version < 2.1.5).