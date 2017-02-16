**SEB 2.2 Preview Version**

Here you can find the current preview build of the next major release of SEB for Windows. Preview builds don't include all the functionality of the final version, they are not tested thoroughly and they are not intended for productive use. You can support us by testing the preview version and give feedback in our forum or by creating an issue here on our GitHub page. 

New in SEB 2.2:
- Fixed that the Windows (file) Explorer was re-started while SEB was running in its kiosk lockdown mode, displaying the Windows Task Bar suddenly.
- SEB config files can now be loaded from servers using authentication (Basic, OAuth etc.) using seb(s):// links. Even indirect links (not containing the config file name with the .seb extension, like for example sebs://example.com/download.php?id=2352) are possible. Therefore a SEB exam config file can be stored for example into the same Moodle course as the quiz. The login session is remembered, therefore students don't have to login twice in SEB if you start SEB/an exam using a seb(s):// link to a config file on an authenticated server. Note: Starting SEB by opening a seb(s):// linked config file from an authenticated server doesn't work yet in this build, only opening such indirect seb(s) links from inside SEB.
- The seb:// and sebs:// URL protocols are now registred in the system and can be used to open SEB with linked settings.
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
- Starting SEB by opening a seb(s):// linked config file from an authenticated server doesn't work yet in this build, only opening such indirect seb(s) links from inside SEB.
- seb2 doesn't yet use SEB settings for setting the browser User Agent.
- seb2 doesn't yet delete the seb2 browser profile folder using the setting "Remove browser profile" (Browser pane in Config Tool). It might be necessary to delete the folder %APPDATA%\SafeExamBrowser\Profiles after updating SEB, because the seb2 browser caches also some of its code files in this folder.
- This build does not yet automatically generate URL filter rules when external additional resources are added. Activate URL filtering and create filter rules manually. 

This document is subject to change, if you're testing SEB 2.2 please check out this document regularly.
