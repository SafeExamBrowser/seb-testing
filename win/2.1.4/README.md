**SEB 2.1.4 for Windows Preview Version**

Here you can find the current pre-release build of the next release of SEB for Windows. You can support us by testing the pre-release version and give feedback in our forum or by creating an issue here on our GitHub page. 

New in SEB 2.1.4 for Windows:
- Fixed a problem which caused the Browser Exam Key to be different when SEB 2.1.3 was updated from an older version than when it was installed freshly. SEB 2.1.4 can be updated from 2.1.1, 2.1.2 or 2.1.3. A direct update from SEB 2.1 might fail, so uninstall SEB 2.1 first using the Windows control panel before installing SEB 2.1.4.
- Monitor Processes is now always active when Disable Explorer Shell is selected as kiosk mode.
- Added Gecko/Firefox setting "browser.display.use_document_fonts = 1", to allow pages to chose their own fonts.
- Fixed a problem when switching keyboards didn't work properly when using specific keyboard layouts (at least when running on Windows 10). Keyboard layout problem with Österreich.
- Fixed: Registry Resetter didn't complain and just did nothing when an inexistent username has been typed in.
- Fixed a problem which caused SEB Windows Service to crash.
- Log SEB version in log file.
- Write log file directly after starting SEB. Logging initially starts in the standard log directory, even if settings define another log file path.