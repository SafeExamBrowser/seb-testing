**SEB for Windows 2.2.2 Preview Version**

Here you can find the current pre-release build of the next release of SEB for Windows. You can support us by testing the pre-release version and give feedback in our forum or by creating an issue here on our GitHub page.

New in SEB 2.2.2pre3 for Windows:

- Another attempt to fix an issue in calculating the Browser Exam Key (BEK) in the SEB Config Tool which happens when the config file contains explicit or implicit seb2 (key whitelistURLFilter and/or urlFilterTrustedContent, not visible in Config Tool) filter rules. As this filter rules could slightly differ (escape characters) or the key urlFilterTrustedContent can be undefined (because it doesn't have a function if URL filtering isn't enabled) and they were not updated in any case before calculating the BEK, it could differ in the SEB Config Tool vs. SEB Client.
- Added a check for detecting additional (irregular) files in SEB's program directory and displaying a warning in that case.
- Fixed an issue when en-US was always selected as spell checking language, even if not allowed in settings, when starting SEB first time after the contents of Firefox Profiles folder were removed.