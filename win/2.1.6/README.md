**SEB 2.1.6 TESTING Version**

Here you can find the current testing build of the next maintenance release of SEB for Windows. Testing builds usually include all the functionality of the final version, but they are not yet tested thoroughly and they are not intended for productive use. You can support us by testing this version and give feedback in our forum or by creating an issue here on our GitHub page. 

New in SEB 2.1.6:

- Improved compatibility with SEB 2.2 generated settings: Removing additionalResources from settings sent to browser.
- Fixed SEB doesn't doesn't finish starting up properly when it can't add some permitted applications (which have been removed but not properly uninstalled).
- Now ignoring SEB/firefox.exe entry from permittedProcesses, which fixes error message when using SEB 2.2 generated settings with SEB 2.1.6.
- Fixed again wrong Browser Exam Key calculation after update by really performing a major update (completely removing old version's files).
- Removed Create new desktop kiosk mode from code which should fix the mouse offset problem introduced by the recent Windows Creators Update.
- Added support for webcams and microphone access with new SEB settings (to SEB Config Tool and seb browser) allowVideoCapture (mapped to media.navigator.video.enabled) and allowAudioCapture (mapped to media.getusermedia.audiocapture.enabled), and set media.navigator.permission.disabled to true (prerequisite for video and audio capture to work in SEB, as the Firefox “allow” alert is not being displayed in SEB).
- Updated seb XUL browser application to current status.
- Set Gecko/Firefox setting "dom.serviceWorkers.enabled" to true.
