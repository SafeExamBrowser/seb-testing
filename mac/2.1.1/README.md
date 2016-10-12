**SEB 2.1.1 for macOS Golden Master Version**

Here you can find the current pre-release build of the next release of SEB for macOS. You can support us by testing the pre-release version and give feedback in our forum or by creating an issue here on our GitHub page. 

New in SEB 2.1.1 for macOS:
- Compatible with macOS 10.12 Sierra.
- Implements support for embedded TLS/SSL & CA certificates and certificate pinning.
- SEB is now using a private clipboard, so utilities running in the background and Universal Clipboard (on macOS 10.12 Sierra) cannot be used to paste text into exams (can be disabled if using third party applications in a securely managed user account).
- WebAudio API is enabled now. 
- Added blocking panels and windows opened by third party tools running in the background.
- Added detection for ScreenSharing.
- Added stopping of AirPlay Display mirroring.
- Now supporting Basic/Digest and NTLM Authentication.
- Loading seb(s):// linked settings from authenticated servers is possible now, even with indirect links (not containing the config file name with the .seb extension, like for example sebs://example.com/download.php?id=2352). The login session is remembered, therefore students don't have to login twice in SEB if you start SEB/an exam using a seb(s):// link to a config file on an authenticatated server.

Fixed bugs:
- On a trackpad supporting Force Touch, the lookup feature (invoked by strongly pressing the trackpad while the cursor is over a word or text selection) was not blocked with the settings option "Allow dictionary look up" disabled.
- Fixed full screen media player app can take over screen if started with the keyboard play key: If iTunes or another media player app supporting media control keyboard keys is maximized to full screen and quit, pressing the play key on the keyboard starts that app and moves it to the foreground, even if SEB is running. The media player app cannot be operated properly as SEB blocks this, but returning to SEB is a bit tricky: Move the mouse cursor to the upper screen edge. Then the window toolbar appears and shows the green window minimize/exit from full screen button on the left. Pressing the green button exits the media player app from full screen and SEB takes the screen over again.
- Fixed a WebKit related bug which occured in older WebKit versions (if running on an older system than OS X 10.11) and with malformatted DOM elements. For example the navigation buttons in a Moodle 1.8 quiz if running SEB 2.1 on OS X 10.10 or older didn't work properly.
