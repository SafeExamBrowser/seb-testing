**SEB for Windows 2.3 Preview Version**

Here you can find the current pre-release build of the next release of SEB for Windows. You can support us by testing the pre-release version and give feedback in our forum or by creating an issue here on our GitHub page.

New in SEB 2.3pre3 for Windows: Golden Master Version, please do final testing and report possible issues ASAP!
- mailto: links are now being ignored.

New in SEB 2.3pre2 for Windows:
- Added zooming of browser windows using the Ctrl +/- shortcuts
- Fixed issue when opening a PDF with a link to be opened in a new browser window (target = _blank or JavaScript open), a second, empty browser window was opened.
- Deactivated printing in the built-in PDF.js viewer, as that opened a security hole.
- Now it's possible to open an embedded PDF file (embedded Additional Resource) when starting a SEB session, instead of a Start URL.
- Fixed bug with last allowed application not starting and all started applications not closing when using SEB without browser.
- SEB now correctly connects to servers using Basic Authentication.
 
New in SEB 2.3pre1 for Windows:
- Fixed issue with quitting SEB and Firefox was running.
- Implemented private clipboard (optional, see Security tab).
- Now the option "Allow downloading and uploading files" is supported in SEB for Windows, at least downloads can be enabled/disabled with this option (Down-/Uploads tab).
- The dialog "Open File With... Safe Exam Browser" is no longer displayed unless the option "Open files after downloading" is enabled (Down-/Uploads tab).
- Enabled SpeechSynthesis API
(Firefox setting media.webspeech.synth.enabled = true), see https://github.com/SafeExamBrowser/seb-win/issues/68


