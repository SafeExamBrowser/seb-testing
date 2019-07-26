**SEB 2.1.13 for iOS Preview Version**

If your are interested in testing SEB for iOS preview versions (using the Apple TestFlight app/service), you can send us your contact details by private message in [our discussion forum](https://sourceforge.net/p/seb/discussion/seb-ios/thread/e7e542a5/?limit=25#feaa/752c) (as GitHub doesn't support private messages) or by email to info at safeexambrowser.org.

Please give feedback through TestFlight, in our forum or by creating an issue here on our GitHub page. 

To be tested:

Version 2.1.13 adds important SEB features which were missing in the iOS version until now. Please test the new SEB 2.1.13 features mentioned below and their compatibility with the desktop versions of Safe Exam Browser. The new Config Key can be tested by using the [prototype for an updated Moodle plugin](https://github.com/SafeExamBrowser/moodle-quizaccess_safeexambrowser) (documentation will be added soon).


**Testing the compatibility of especially this beta version with all exam systems is crucial, because it uses some custom networking and web request handling code (a custom web cache and if the Browser Exam/Config Key or embedded SSL certificates are used, a custom URL loading protocol).**

As the SEB for iOS app usually is updated automatically on student devices as soon as a new version is available in the App Store, **it's important that SEB users test the beta version and report issues BEFORE the final version is released**. So if you are using SEB for iOS in your institution or distribute it with your own assessment solution, please contribute to the improvement of the SEB open source software by participating in our beta version testing. **At the same time, participating in beta testing helps you to avoid possible issues when the new version is released publicly.**

**PLEASE NOTE: SEB 2.1.13 for iOS uses a different policy to decide if it can be reconfigured when a seb(s) URL or a .seb config file is opened:** When running in secure mode (a quit password is set in the currently active settings, which invokes AAC/the selected Single App Mode), SEB 2.1.13 cannot be reconfigured, even if it's using persisted client settings. Earlier versions could always be reconfigured when using client settings. If you want to allow reconfiguring SEB by opening a seb(s) URL while running in secure mode, then you need to use the  "Allow Reconfiguring" and "Reconfiguring Config URL" options in Settings/Exam Session. This new policy for reconfiguring will also be introduced to upcoming desktop versions of SEB.


New in build 11892: SEB 2.1.13 Release Candidate
- Stop media player audio after its web view was closed.
- Don't display error "Plug-in handled load".
- Fixed that the error "Frame load interrupted" could be displayed when a blocked URL was opened:
Happened when a forwarded URL was blocked by a URL filter. Fixed by ignoring this load error 102.


New in build 11889
- Fixed Browser Exam Key/security issue when running on iOS 9/10.


New in build 11888
- As the Reload button should only be displayed in one location: Fixed that configuration changes for visibility of Reload button in dock didn't remove it in the browser toolbar.


New in build 11887
- Improved implementation of the Browser Exam Key: The Browser Exam Key (BEK) depends on SEB's code signature and the current SEB config. Copy the value to the according field in the quiz settings of a compatible exam system. SEB on each platform generates another BEK, even if the same SEB config is used. Different versions of SEB for iOS generate the same BEK, as long as the same SEB config file is used. This is crucial, as otherwise an update of SEB through the App Store, which can happen at any time, would prevent access to exams protected with the BEK. **IMPORTANT: Consider the fact that an update of SEB for iOS on unmanaged iOS devices/BYOD can happen at any time! In case you're checking for specific SEB versions in your exam system integration: For the iOS version only check for an allowed minimum version!** 
 
- Moved display and sharing of current Browser Exam Key and Config Key to separate page in Settings / Exam Session / Share Keys. There you can also see if permanent setting options in the currently opened SEB config are unaltered or have been changed. In the latter case, the message "Config was modified, keys won't match original state!" is displayed.
- Added setting options to share Browser Exam Key (BEK) and/OR Config Key (CK) either together with a config file containing current settings or without the config. The later option doesn't modify the currently loaded config, so you don't need to update the config file if you already placed it on a server and used it with other SEB versions and the BEK. The key(s) are also copied to the clipboard when closing Settings (so an exam admin can easily paste them to the according quiz settings). If only one of the keys is shared (most commonly only the BEK needs to be manually copy-pasted to exam settings), then the string copied to the pasteboard contains only the key without description ("Browser Exam Key: ..." or "Config Key: ...").

- Added setting option to allow media auto play. By default media doesn't auto play, unless you allow it with the option Settings / Browser Features / Media Autoplay.
- Added setting options to control if video can be played inline on a web page or only in full screen. There are two separate settings for "Allow Inline Playback on iPad" (enabled by default) and "Allow Inline Playback on iPhone" (disabled by default) in Settings / Browser Features. Please note that by disabling this option, HTML5 video players are forced to use the iOS user interface for controlling playback, which often offers much better usability than custom playback interfaces and guarantees proper full screen presentation. 
- Implemented functionality and setting option "Allow Picture in Picture Video". On iPad devices supporting PiP, the video plays in a movable and resizable overlay window. If not running SEB in Single App Mode (open book exams, using other apps in exams on managed devices), PiP video keeps playing even if switching to other apps.
- SEB now supports Slide Over and Split View when not running in Single App Mode (open book exams, using other apps in exams on managed devices).
- Added iOS 13 to the "Allow Running on iOS Beta" option.
- Fixed handling MDM server config (Managed Configuration), when it's being send repeatedly and was causing "Loading New Settings Not Allowed" alert being displayed when an exam was running. Also fixed that Settings were closed when they were displayed while SEB was backgrounded and after the user switched back to SEB. In this case now an alert is displayed asking if the received MDM settings should be applied (and in-app Settings closed).
- Fixed lock screen issue.
- Moved option "Allow QR Code Config" from Security to Config File Settings page.


New in build 11870:
- New identities for encrypting and decrypting config files (containing a self signed certificate and random private key) can now be easily created in Settings/Network/Certificates/Choose Identity/Create New…
- Identity certificates for decrypting SEB exam configs can be embedded into client configs (see Settings/Network/Certificates/Choose Identity). 
- Identities can be removed from the Keychain (see Settings/Network/Certificates/Choose Identity).
- Now Automatically creating and embedding an identity when the option is enabled in Settings/Config File (available when editing client config files). 
- Now auto-selecting latest created or imported identity for encrypting exam configs when the option is enabled in Settings/Config File.
- When sharing an identity-encrypted config file, the text "encrypted with identity certificate '...'" is added to the description string.
- Added "more Actions"/"+" button to in-app-settings root view with options "Create Exam Settings" and "Reset to Default Settings" (when in client config) and "Revert to Client Settings" (when in exam config).
- SEB can now also open .seb config files from iCloud Drive (Files App)
- Added About SEB button (as SEB icon) to the Initial Configuration Assistant view, so the "Send SEB Log to Developers" link is accessible also when the assistant is visible.
- Fixed crash when dragging elements in UIWebView. Unfortunately UIWebView doesn't support modern HTML5 Drag and Drop, currently you have to use older methods.
- Fixed: Wrong error message was displayed when identity certificate for decrypting settings wasn't found in Keychain. Also no longer searching for a Universal/Deep Link config in this case.
- Moved option "
- Fixed crash when calculating Config Key on corrupted settings.
- Fixed crash when reading identities which don't have email addresses in their certificate.


New in build 11860:
- Support for encrypting config files with identity certificates. These have to be distributed by embedding them into a client config file (currently identities need to be embedded in a desktop version of SEB).
- Setting for log level is now functional (Settings/Security/Logging/Log Level).
- Now logging events in the custom URL loading protocol, when the log level is set to Verbose.  
- Now displaying an alert when a file (from website generated data) was downloaded successfully.
- Fixed crash in custom URL loading protocol.


New in build 11850:
- SEB for iOS now supports downloading files. Currently only website generated files (using the [data: scheme](https://en.wikipedia.org/wiki/Data_URI_scheme)) can be downloaded. This feature is meant for saving encrypted exam results in case there is no network connection. Those files can be accessed in the Files app ("On My iPad/iPhone" location) and by using iTunes.
- Added setting "Allow Downloading" (settings key: allowDownUploads, default value: false) to in-app settings on a new root-level settings page "Downloads".
- Moved and renamed setting "Download & Open Config Files" to the new settings page "Downloads".
- Fixed issue not loading SEB config when seb(s) URL not containing .seb is used to start SEB.
- Now also sending Config Key and Browser Exam Key (BEK) when using http.
- Now downloading SEB config data asynchronously to avoid SEB freezing when there are issues while downloading the data.
- Fixed allowed minimum iOS version settings option: Changing minor and patch versions in in-app settings didn't work.
- Comparing current iOS version with the allowed minimum version didn't work correctly.


New in build 11840:
- The Browser Exam Key and the new Config Key hash values are generated by SEB for iOS and send with HTTP requests (if enabled in Settings/Exam Session). Compatible assessment systems can use these hash values to verify that an exam is accessed with an approved version of SEB and deny access to the exam if a regular browser is used, if SEB is used with wrong settings or if a manipulated version of SEB is used.
- SEB for iOS generates the same Config Key for a SEB config file generated with SEB for macOS 2.1.4pre2 or newer. The config key doesn't change if an updated SEB version is used (even if a new SEB version introduces new setting keys).
- SEB for iOS now supports the URL filter feature to restrict access to websites/pages/web resources. Use the desktop versions of SEB to generate config files containing such URL filter rules.
- SEB 2.1.13 uses the full native resolution when running on the new iPad Pro devices with Face ID.
- SEB for iOS now saves log files according to the options in Settings/Security/Logging (enable logging, log levels). Those logs can be emailed using a button accessible in the "About SEB" view (scroll to the bottom of the copyright text) to the SEB developers or to yourself.
- Improved reliability of MDM Managed Configuration, for example when receiving a new config from the server when SEB isn't running, in the background or if alerts, in-app settings or initial configuration assistant are displayed in SEB.
- Added options for links requesting to open in new tab (see Settings/Browser Features), compatible with SEB for macOS.
- The Quit Link feature can now optionally restart an exam session instead of quitting it (Settings/Exam Session).
- Exam sessions can now optionally be reconfigured (see Settings/Exam Session) before having to first quit the running exam session.
- Clearing of session cookies can now optionally be disabled, allowing users to stay logged in if they already were in a previous session (Settings/Exam Session).
- Deep linking for exams now also works with sebs:// links (in addition to Universal Links, see Settings/Exam Session).