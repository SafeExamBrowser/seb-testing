**SEB 2.1.1 for macOS Preview Version**

Here you can find the current preview build of the next release of SEB for macOS. Preview builds don't include all the functionality of the final version, they are not tested thoroughly and they are not intended for productive use. You can support us by testing the preview version and give feedback in our forum or by creating an issue here on our GitHub page. 

New in SEB 2.1.1 for macOS:
This build fixes security issues (force touch lookup, play keyboard button can start full screen player app, admin password when opening unencrypted settings for editing), and a WebKit related bug. Implements support for embedded TLS/SSL & CA certificates and certificate pinning, WebAudio API and loading seb(s):// linked settings from authenticated servers.
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
- On a trackpad supporting Force Touch, the lookup feature (invoked by strongly pressing the trackpad while the cursor is over a word or text selection) was not blocked with the settings option "Allow dictionary look up" disabled.
- Fixed full screen media player app can take over screen if started with the keyboard play key: If iTunes or another media player app supporting media control keyboard keys is maximized to full screen and quit, pressing the play key on the keyboard starts that app and moves it to the foreground, even if SEB is running. The media player app cannot be operated properly as SEB blocks this, but returning to SEB is a bit tricky: Move the mouse cursor to the upper screen edge. Then the window toolbar appears and shows the green window minimize/exit from full screen button on the left. Pressing the green button exits the media player app from full screen and SEB takes the screen over again.
- 

Known limitations:
- seb2 doesn't yet use SEB settings for setting the browser User Agent.
- seb2 doesn't yet delete the seb2 browser profile folder using the setting "Remove browser profile" (Browser pane in Config Tool). It might be necessary to delete the folder %APPDATA%\SafeExamBrowser\Profiles after updating SEB, because the seb2 browser caches also some of its code files in this folder.
- The seb:// and sebs:// URL protocols are not yet registred in the system in this preview version build. 
- This build does not yet automatically generate URL filter rules when external additional resources are added. Activate URL filtering and create filter rules manually. 

This document is subject to change, if you're testing SEB 2.2 please check out this document regularly.
