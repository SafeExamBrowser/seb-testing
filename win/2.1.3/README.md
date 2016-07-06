**Safe Exam Browser 2.1.3**

Testing Build 2

Changes:
- Added support for system proxy settings in XUL seb.
- SEB Windows service didn't start properly on some machines (SID could not be determined using the user name).
- Fixed URL of SEBWindowsServiceWCF to avoid collisions with other WCF services.
- Possibly the two fixes above improve stability of resetting registry settings.
- Fixed wrong version number in SEB installer.
- Now disabling "Monitor processes" option in Applications tab, when kiosk mode 'Disable Explorer Shell' is active (because then processes are anyways monitored). 

Resolved issues from previous build:
- If updating from SEB 2.1.2, the SEB installer failed to update some files belonging to SEB Service, causing the SEB Windows Service not to start. 

Known issues in this build:
- Current versions of Internet Explorer, Edge and Windows 10 complain about an invalid signature of the SEB installer when downloading or starting it. Reason: Windows doesn't accept executables signed with code signing certificates using a SHA-1 signature since a security update from January 12, 2016 (if the executable was signed using SHA-1 after this date). Build 2 is actually signed with a new code signing certificate with a SHA-256 signature, but the root CA used by the certificate provider is still using a SHA-1 signature. It looks like Windows/IE/Edge expect the whole certificate chain to be signed with SHA-2. So we are again waiting for a new, correctly working signing certificate.
