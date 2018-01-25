**SEB 2.1.3 for macOS Preview Version**

Here you can find the current pre-release build of the next release of SEB for macOS. You can support us by testing the pre-release version and give feedback in our forum or by creating an issue here on our GitHub page. 

New in SEB 2.1.3 for macOS:
- Now blocking Predictive Text in TouchBar during an exam.
- Fixed that double clicking a .seb config file several times could lock SEB.
- The About SEB splash screen now cannot hide alerts and lock SEB if those were displayed modally.
- The screen sharing detector now also works correctly when connecting to a Mac using Apple ID (Back to My Mac).
- Added checkbox to lock screen to override security check and unlock SEB, even if screen sharing is still active. Displaying info about overriding security check in HUD (in red text color).
- Fixed lock screen windows could be opened twice (for screen sharing and user switch) which would make it impossible to unlock again.
- Fixed names of running processes in log were truncated after 16 characters.
- Now adding "Version xx.x.x" string after "Safari" in user agent string.
- Improved logging when starting SEB: Now starting to log (with log level Debug and at standard log file path) regardless of current settings directly after SEB starts up, before local persistent settings are initialized.
- Again fixed a bug when SEB could kill itself when a space switch occurred, this time correctly.
- Fixed opening seb(s):// link wasn't working when temporary browser window (for authentication) was open and SEB was restarted after editing preferences.
- Added one point to menu bar height to keep a black edge between menu bar and browser window.
- Fixed a compatibility issue which caused SEB 2.1.2 to crash immediately when started on OS X 10.7.