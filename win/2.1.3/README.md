**Safe Exam Browser 2.1.3**

Testing Build 1

Changes:
- Added support for system proxy settings in XUL seb.
- SEB Windows service didn't start properly on some machines (SID could not be determined using the user name).
- Fixed URL of SEBWindowsServiceWCF to avoid collisions with other WCF services.
- Possibly the two fixes above improve stability of resetting registry settings.
- Fixed wrong version number in SEB installer.
- Now disabling "Monitor processes" option in Applications tab, when kiosk mode 'Disable Explorer Shell' is active (because then processes are anyways monitored). 

Known issues in this build:
- Current versions of Internet Explorer, Edge and Windows 10 complain about an invalid signature of the SEB installer when downloading or starting it. Reason: Windows doesn't accept executables signed with code signing certificates using a SHA-1 signature since a security update from January 12, 2016 (if the executable was signed using SHA-1 after this date). We are waiting for a new signing certificate with a SHA-2 signature.
- If updating from SEB 2.1.2, the SEB installer fails to update some files belonging to SEB Service, causing the SEB Windows Service not to start. Workaround: Uninstall older SEB versions manually before installing this build of SEB 2.1.3.
