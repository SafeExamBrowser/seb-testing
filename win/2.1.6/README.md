**SEB 2.1.6 Preview Version**

Here you can find the current preview build of the next major release of SEB for Windows. Preview builds don't include all the functionality of the final version, they are not tested thoroughly and they are not intended for productive use. You can support us by testing the preview version and give feedback in our forum or by creating an issue here on our GitHub page. 

New in SEB 2.1.6:

- Removed Create new desktop kiosk mode from code which should fix the mouse offset problem introduced by the recent Windows Creators Update.
- Added new SEB settings (to SEB Config Tool and seb browser) allowVideoCapture (mapped to media.navigator.video.enabled) and allowAudioCapture (mapped to media.getusermedia.audiocapture.enabled), and set media.navigator.permission.disabled to true (prerequisite for video and audio capture to work in SEB, as the Firefox “allow” alert is not being displayed in SEB).
- Updated seb XUL browser application to current status.
- Set Gecko/Firefox setting "dom.serviceWorkers.enabled" to true.
