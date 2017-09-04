**SEB 2.2 Preview Version**

Here you can find the current preview build of the next major release of SEB for Windows. Preview builds don't include all the functionality of the final version, they are not tested thoroughly and they are not intended for productive use. You can support us by testing the preview version and give feedback in our forum or by creating an issue here on our GitHub page. 

New in SEB 2.2pre2:

- Changed reload in seb2 from hard reload to soft reload (to not break Service Worker when offline).
- Added settings allowVideoCapture, allowAudioCapture to Config Tool / Browser. 
- Removed SEB for macOS settings in Config Tool / Browser for new browser windows opened by JavaScript/Plugins.
- Updated seb2 XUL browser application to current status.
- Updated embedded Firefox to version 52.3.0 ESR.
- Browser windows without title should now be displayed correctly in window chooser and be correctly reloaded with the reload button in the task bar.
- Attempt to fix the issue happening when deleting the temporary directory.
- Enhanced SEB Windows Service implementation with fallback file for Registry settings and added more logging information, to prevent that lock, switch user, sign out, change a password and Task Manager are missing in the Windows Security Screen invoked with Ctrl-Alt-Del.
- Added improved logging for the embedded browser. Note: The log path cannot be changed in exam settings, SEB now uses always the path (and log enable option) which is configured in client config.
- Fixed: Quitting running applications, either when starting SEB (if they are configured as permitted applications) or when quitting SEB (running permitted applications) failed when these applications consisted of more than one process (have a window handling process) or due to a bug in the quitting processes function.
- Again attempting to fix crash when quitting SEB by disabling WndProc of TaskbarToolStrip on application shutdown.
- Removed starting seb2/Firefox with -silent argument again, as it doesn't seem to be necessary to explicitly create seb2/Firefox profile.
- Added some Firefox settings to improve Service Worker support.
- Created new installer using the (commercial) InstallShield authoring solution, as in SEB 2.1.x. Apparently the WiX installer still has some issues (file type association not being removed when uninstalling SEB 2.2, SEB 2.1.x entry in the Windows Programs Control Panel isn't removed when SEB 2.2 is updated from SEB 2.1.x. Also we are still missing an install bundle which would install .NET 4.5 automatically on machines running Windows 7.
- Updated embedded browser to Firefox 52.2.1 ESR (which will receive security updates until June 2018). This is the last version which is compatible with the seb2 XUL browser engine used in SEB 2.2. A future new major release of SEB will be using the Chromium browser engine. 
- SEB 2.2 now supports Service Workers.
- Changed default value for setting removeBrowserProfile to false.
- Removed message box displayed when cleaning of temporary directory failed.
- Set Gecko/Firefox setting "dom.serviceWorkers.enabled" to true.
- In the native HTML full screen mode, the SEB task bar is also hidden now. Please note: You have to enable the "Esc" key in SEB settings if full screen mode on your website can only be exit using the key (otherwise provide a button on the webpage!).
- Default browser agents (desktop and touch mode) now use the default user agent string of the embedded Firefox browser, therefore the user agent reflect the operating system version SEB is running on and the used Firefox version. 
- Added "Firefox/xx" to the default browser user agent strings for better compatibility.
- In the "iPad" setting option for the user agent for touch/tablet mode, the default iPad user agent string can be edited in the Config Tool / Browser pane.
- Fixed that for some third party applications new instances were started when clicking the icon in the task bar (instead switching to the window of the already running instance).
- Fixed: Already running instances of permitted applications were not quit when SEB starts and were accessible inside SEB. Also fixed this for prohibited applications.
- Fixed some config tool UI issues: Radio buttons for Zoom Page/Text and User Agent were sometimes not set properly after loading a new config file, main browser window size wasn't disabled when using full screen mode.
- Fixed in Network/Filter: If editing a filter rule (block/allow), the Config Tool didn't save this edited rule when using commands Save, Save As, closing the Config Tool, Open Settings (with button, menu and drag-and-drop), Revert Settings to Default/Local Client/Last Opened, Use Current Settings to Edit Duplicate/Configure Client/Apply and Start SEB.
- In the following cases also added checking for unconfirmed passwords: Open Settings (with button, menu and drag-and-drop), Revert Settings to Default/Local Client/Last Opened, Use Current Settings to Edit Duplicate/Configure Client/Apply and Start SEB.
- Starting SEB by opening a seb(s):// linked config file from a server secured with Basic Authentication works now as well.
- Now monitoring processes is always automatically enabled except when "None (for debugging only)" kiosk mode is selected.
- Updated embedded browser to Firefox 51.0.1.
- Browser Exam Key is now sent in requests. User interface for this option in the SEB Config Tool Exam tab makes it clearer that you need to enable the option for the key actually being sent in HTTP requests.
- Starting SEB by opening a seb(s):// linked config file from an OAuth authenticated server works now, with limitations (might break the Quit Link functionality).
- SEB now looks for X.509 identity certificates for decrypting an identity-encrypted config file also in the "Trusted People" store in the Windows Certificate Store (in addition to the default "Personal" store). On managed computers this allows to deploy the identity certificate to the "Local Machine/Trusted People" store when installing SEB in an administrator account. The certificate will then also be available in the "Current User/Trusted People" stores of all current users on that machine.
- Added Gecko/Firefox setting browser.display.use_document_fonts = 1 (as in SEB 2.1.4).
- Made calculation of Browser Exam Key more stable by excluding .gitignore and .DS_Store files from hash and by sorting files alphabetically.
- Added new asymmetric/symmetric encryption for config files using identity certificate: First encrypt a randomly generated symmetric key using the X.509 certificate, which is then used to encrypt the config data (for better performance when decrypting certificate encrypted config files).
- Added new option to Config Tool / Config File pane to use old asymmetric-only encryption (for compatibility with SEB < 2.2).
- Added new settings option in Browser pane "Allow navigating in additional browser windows". This allows to separately allow browsing back/forward in new browser windows (for example for additional resources), even if it should not be allowed in the main browser window where the exam is running. 
- SEB config files can now be loaded from servers using authentication (Basic, OAuth etc.) using seb(s):// links. Even indirect links (not containing the config file name with the .seb extension, like for example sebs://example.com/download.php?id=2352) are possible. Therefore a SEB exam config file can be stored for example into the same Moodle course as the quiz. The login session is remembered, therefore students don't have to login twice in SEB if you start SEB/an exam using a seb(s):// link to a config file on an authenticated server. Note: Starting SEB by opening a seb(s):// linked config file from an authenticated server doesn't work yet in this build, only opening such indirect seb(s) links from inside SEB.
- The seb:// and sebs:// URL protocols are now registered in the system and can be used to open SEB with linked settings.
- SEB now deletes the browser profile folder using the setting "Remove browser profile" (Browser pane in Config Tool). The browser profile folder is now also deleted when updating SEB, to prevent problems with not updated, cached browser modules.
- SEB now uses the config options for setting the browser User Agent.
- Added AudioControl Component to SEB task bar, which allows to increase/decrease and mute system audio volume. Audio can be muted or the audio level preset when starting SEB. 
- Adjusted additional resource submenu handling: Now shows on MouseOver and opens the resource on click.
- Additional resources on root level display an icon in the task bar
- Added browser window suffix setting (Browser tab)
- Added confirm quit link setting (Exam tab)
- Replaced the deprecated Mozilla XULRunner browser engine by a full Firefox browser (which is nevertheless running in the same mode with reduced functionality).
- Refactored seb2 XUL browser app.
- Support for additional resources, which can be external (defined by a URL) or embedded into the SEB config file. An embedded resource can be one file or a whole directory with subdirectories, which can either be opened and displayed by the SEB browser or one of the permitted applications.
- SEB can load one of the embedded resources instead of an "Start URL". With this feature pure offline exams can be done if using an offline exam player (for example a HTLM5 exam app).
- Added a page loading (network activity) indicator.
- Added a browser window toolbar, similar to SEB for Mac OS X.

Fixed bugs:
- Again fixed a a bug  which sometimes caused SEB to crash while exiting, which was caused by the Create New Desktop kiosk mode and the therefore omitted "STAThread" command (this time properly). "STAThread" is now active, which should increase stability of SEB while quitting and starting (sometimes the "Confirm Quitting" message box wasn't displayed and SEB seemed frozen when quitting).
- Fixed on-screen keyboard wasn't displayed in latest versions of Windows 10. "Tablet Mode" needs to be activated in the system. If it isn't, the keyboard icon in the SEB task bar is deactivated and the tooltip indicates that "Tablet Mode" needs to be active and the hardware keyboard detached. 	
- Fixed Bug unable to start WebSocketsServer / WebSocket is blocked.
- Fixed that the Windows (file) Explorer was re-started while SEB was running in its kiosk lockdown mode, displaying the Windows Task Bar suddenly.
- Fixed bug when some keyboard layouts were not switched properly (and other, actually in Windows settings not activated layouts were used) when running SEB on Windows 10.
- SEB Registry Resetter now exits when a non-existing/wrong user name is entered.
- Added another method to find out the SID of the current user and send it to the SEBWindowsService. This is an addition to the username, because the translation from username to SID inside the Service sometimes fails.
- Fixed auto open additional resource behavior when SEB is the launcher.
- Added update mechanism in WiX Installer to fix updates of SEB 2.2 to another 2.2 build.
- Fixed various seb2 bugs
- Favicons for external additional resources are now loaded in the
config tool.
- The desktop background picture is now also removed on PCs running Windows 7.
- If SEB cannot terminate or force quit prohibited applications (Config Tool / Applications / Prohibited Processes) because they are running with other user permissions, then the exam is blocked and SEB asks to enter the quit/restart password (which exam supervisors/supporters should know) to continue.

Known limitations:
- This build does not yet automatically generate URL filter rules when external additional resources are added. Activate URL filtering and create filter rules manually. 

This document is subject to change, if you're testing SEB 2.2 please check out this document regularly.
