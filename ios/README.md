This build is a release candidate. Please test this version asap with your exams/assessment systems, as we will release the final version in the App Store in a few days.

New in build 12203:
- SEBMAC-225 No longer displaying "Do you want to close Settings and apply this managed configuration?" after receiving the same config from the MDM server as currently is active.

New in build 12173:
- SEBMAC-225 Preventing error "Loading New Settings Not Allowed! ... is already running in exam mode ..." after "Do you want to abort opening Settings and apply this managed configuration?" was confirmed.
- SEBMAC-225 Try to apply MDM config later, after it wasn't applied in Settings after dialog "Do you want to close Settings and apply this managed configuration?".
- SEBMAC-225 Fix applying MDM (client) configuration when device with iOS < 13 is put to sleep during AAC and then woken up again fails with error "Loading New Settings Not Allowed! ... is already running in exam mode ...".
- SEBMAC-225 Fix closing Settings after according dialog was confirmed with "Ok" after receiving different client config from MDM server and SEB was just started.
- Changed year in copyright to 2020.

New in build 12157:
- SEBMAC-225 Fixed applying MDM reconfiguration, now it works according to specification.

New in build 12055:
- SEBMAC-225 Added another condition for applying MDM app configuration: Only reconfigure when received settings actually differ from current settings. Also try to reconfigure back to MDM app config which was received already before. Make sure to lock MDM reconfiguration as soon as the MDM config was received (because the MDM/iOS is sending repeated events with the same received configuration). 

New in build 12051:
- SEBMAC-224 Fixed displaying a lock screen after a student closed their iPad case and then opened it again (iOS < 13), which was also displayed when starting an exam using a .seb config file or seb(s) link from another app.

New in build 12050:
- SEBMAC-235 Allow to open SEB config files from iCloud Drive (using Files app).
- SEBMAC-151 Listen for and block attempts to record the screen, if setting enablePrintScreen is false (InAppSettings: Security / Allow Screen Capture).
- SEBMAC-224 Display a lock screen after a student closed their iPad case and then opened it again (iOS < 13). This is only displayed when the new setting mobileSleepModeLockScreen is true (InAppSettings: Security / Lock Screen After Sleep Mode).
Fixed issue that when locking an exam, wrong (previous) lock screen message could have been displayed.
- SEBMAC-225 Changed policy when reconfiguring with MDM settings, to prevent settings are overwritten by MDM or SEB reconfigures to client settings during a running exam, even when no plist is configured in the MDM:
1) When reconfiguring (back) to client settings
2) When opening in-app settings, SEB indicates if MDM settings were received and asks if those should be applied.
3) When SEB is running with client settings, there is only one browser tab (with the exam web page) open and the current URL (still) is the Start URL.
4) When secure client settings were quit and SEB is waiting to start another session.
5) When returning back to the SEB app, cases 3 or 4 apply or in-app settings are open (ask user if MDM settings should be applied)
- SEBMAC-228 Replace key string mobileShowSettings with string showSettingsInApp in default settings.
- SEBMAC-229 Fixed value type for "Show URLs: Always" in In-App-Setting.
- SEBMAC-234 Added error message in case AAC couldn't be started properly on older iOS versions.

New in build 11996:
- SEBMAC-227 Make UI accessible by VoiceOver: Added accessibility labels and hints to buttons and excluded unnecessary UI elements. 
- SEBMAC-227 After opening left side menu, move VoiceOver focus to the first browser tab entry.
- SEBMAC-227 Added keyboard shortcut to toggle left side menu (show/hide) Command-M for better accessibility.
- SEBMAC-227 Changed left side menu "SafeExamBrowser version number" title to a button which closes the side menu for better accessibility.
- SEBMAC-227 Activated "dynamic type" for most UI strings.
- SEBMAC-221 Fixed wrong Config Key was calculated when new default settings containing dictionaries were added in new SEB version. Removed unnecessary double calculating of new Browser Exam and Config Key after opening new config file.
- SEBMAC-225 Attempting to fix: Settings or are overwritten by MDM, even when no plist is configured in the MDM.
- SEBMAC-199 Replaced various error and warning log messages (which weren't actually justified there) with info and debug level.
- SEBMAC-229 Fixed setting Browser Features / "Show URLs: Always" couldn't be selected in In-App-Settings and activating this option wasn't showing the page URL in the side menu.

New in build 11947:
- SEBMAC-215 Implemented hardware keyboard shortcuts (Ctrl-Tab/Shift-Ctrl-Tab) to switch browser tabs.
- SEBMAC-212 Implemented separate settings to clear cookies when starting/ending session (keys examSessionClearCookiesOnStart / examSessionClearCookiesOnEnd). This prevents security issues with users staying logged-in after reconfiguring SEB with new settings, if this wasn't actually intended.
- SEBMAC-104 Fixed URL filter doesn't treat query strings consistently (Windows/macOS - iOS).
- SEBMAC-157 If checking server trust with embedded certificates, resources in subdomains of already trusted domains are now trusted as well, according to behavior in other standard browsers.
