**SEB 2.1.5 for Windows Pre-Release Version**

Here you can find the current pre-release build of the next release of SEB for Windows. You can support us by testing the pre-release version and give feedback in our forum or by creating an issue here on our GitHub page. 

New in SEB 2.1.5 for Windows:
- Fixed for some third party applications new instances were started when clicking the icon in the task bar.
- Fixed already running instances of permitted applications were not quit when SEB starts and were accessible inside SEB.
- Also fixed this with prohibited applications.
- Fixed some config tool UI issues: Radio buttons for Zoom Page/Text and User Agent were sometimes not set properly after loading a new config file, main browser window size wasn't disabled when using full screen mode.
- Added Gecko setting for HTTP2 (network.http.spdy.enabled.http2) to XUL seb config file prefs.js. Currently not changing default true to false, despite some unconfirmed information that HTTP2 doesn’t work in Gecko <= 48. Please let us know if you have a reproducible case where HTTP2 doesn't work with SEB 2.1.5.
- Added MIME type application/seb to the .seb file type which the installer registers.
- Fixed in Network/Filter: If editing a filter rule (block/allow), the Config Tool doesn't save this edited rule when using commands Save, Save As, closing the Config Tool. In the following cases in addition also added checking for unconfirmed passwords: Open Settings (with button, menu and drag-and-drop), Revert Settings to Default/Local Client/Last Opened, Use Current Settings to Edit Duplicate/Configure Client/Apply and Start SEB.
