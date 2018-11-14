**SEB for Windows 2.2.3 Preview Version**

Here you can find the current pre-release build of the next release of SEB for Windows. You can support us by testing the pre-release version and give feedback in our forum or by creating an issue here on our GitHub page.

New in SEB 2.2.3pre2 for Windows:
- Settings option to switch off detector for RDP/remote session (key allowScreenSharing) now also is considered when changing Registry setting for terminal sessions.

New in SEB 2.2.3pre1 for Windows:

- Fixed an issue in calculating the Browser Exam Key (BEK): Now sorting browser files for hashing with culture invariant string comparer to avoid problem with Swedish (order of letters "w" and "v" reversed) and probably Turkish locale settings. Because of the wrong alphabetic sorting, a different BEK was calculated on Windows set to such languages (locales) since SEB 2.2 and the check for detecting additional (irregular) files in SEB's program directory displayed a warning in SEB 2.2.2.
- Added settings option to switch off detector for RDP/remote session (key allowScreenSharing)
- Added settings options for Use private clipboard and all settings from macOS 2.1.3 version to Config Tool / Security pane.