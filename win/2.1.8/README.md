**SEB 2.1.8.1 GM2 Beta Testing Version**

Here you can find the current beta testing build of the next minor release of SEB for Windows. Testing builds are not intended for productive use. Beta builds contain the final functionality of the release. You can support us by testing this version and give feedback in our forum or by creating an issue here on our GitHub page. 

New in SEB 2.1.8:

- Added logging commands around WMI queries to be able to find out exactly where possible delays happen.
- Added GotoMeetingWinStore to strictly prohibited processes, moved CamRecorder to default prohibited processes, removed some unnecessary processes.
- Improved performance of checking for running processes during startup.
- Logging all processes which are running when starting / reconfiguring SEB
- Improved closing of processes which are not allowed to run.
- Added Camtasia Recorder to strictly not permitted applications.
- Changed version number of SEB client to 2.1.8.1 (because 2.1.8 was shortly available for download before having to be pulled back due to the discovered severe issue).
- Changed wording in message box "Permitted Processes Are Already Running”.
- Fixed quitting SEB doesn't quit some permitted processes like Acrobat.
- Fixed that the wrong permitted process was automatically started (with autostart property set) when the SEB browser is deactivated.
- Added log information whether a permitted process has the "autostart" property set and will be automatically started together with SEB.- Process monitoring is now always active if either of the two kiosk modes is set.
- Fixed a security issue, now checking for SEB windows uses original filename as well.
- Adding strictly prohibited default processes (screen sharing and communication tools) unconditionally to settings, default (browser) processes only in Disable Explorer Shell kiosk mode.
- Now removing prohibited default processes in SEB Config Tool conditionally (if user confirm) from settings when loading config file which has Create new desktop kiosk mode set or when switching to Create new desktop (in Security tab).
- Now logging all SEB files which are used for generating the Browser Exam Key.
- Added the sebs protocol to MIME types which the seb browser loads without asking the user what to do with it.
- Fixed dialog for entering settings password (if displayed when starting SEB) had a wrong scale if the system DPI ratio was different than 100%.
- Added monitoring of Windows Explorer to prevent rare cases when explorer.exe was restarted and the shortcuts Win+Tab and Win+D were working.
- Re-integrated the "Create New Desktop" kiosk mode and declared dpi-awareness in attempt to resolve mouse pointer offset.