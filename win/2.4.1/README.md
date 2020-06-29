**SEB for Windows 2.4.1 Preview Version**

Here you can find the current pre-release build of the next release of SEB for Windows. You can support us by testing the pre-release version and give feedback in our forum or by creating an issue here on our GitHub page.

New in SEB 2.4.1 for Windows (second pre-build which probably is the Golden Master):
- Fixed issue when reconfiguring with seb(s) link and old browser window stayed open, together with the Firefox file open dialog.
- Implemented fix for VMware issue: The registry values will now only be set if the active configuration explicitly says so.
- Added Zoom to list of prohibited applications. If you want to use Zoom together with SEB, you have to set its "Active" property to false (Applications / Prohibited Processes).
- Added expansion of environment variables in path of permitted processes.