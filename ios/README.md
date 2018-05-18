**SEB 2.1.10 for iOS Preview Version**

You can send us your contact details if your are interested in testing SEB for iOS preview versions (using the Apple TestFlight app/service):


. Please give feedback through TestFlight, in our forum or by creating an issue here on our GitHub page. 

New in build 10260:
- Fixed: When SEB was started with opening a seb(s):// link and after the exam was quit: No initial assistant view was displayed (only a white empty page), starting another exam with a seb(s):// link didn't work anymore. Tapping "Back to Start" button in this state crashed the app.
- Show status bar (with battery indicator etc.) by default (white text on black background).
- Added setting option "Download/Open SEB Config Files" to "Security".
- Start URL web page from client config was unnecessarily loaded when SEB was started by a seb(s):// link.
- Fixed "Restart Session" alert was also displayed even if new settings didn't have a secure mode set.
- Now handling correctly when user leaves SEB while the "No kiosk mode available" alert is displayed.
- Changed "Loading Settings" settings password dialog title depending on mode starting exams/configuring client to "Loading Exam" / "Loading Client Settings" to clarify what is happening. 

New in build 10265:
• Fixed: "Load Error - NSURLErrorDomain error -999" was displayed sometimes, even though the web page loaded properly.

