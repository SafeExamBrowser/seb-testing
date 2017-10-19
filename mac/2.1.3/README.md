**SEB 2.1.3 for macOS Preview Version**

Here you can find the current pre-release build of the next release of SEB for macOS. You can support us by testing the pre-release version and give feedback in our forum or by creating an issue here on our GitHub page. 

New in SEB 2.1.3 for macOS:

- New settings-only hash key, called "Config Key". This is a hash over all config key/value pairs. This new key is SEB version and also platform independent. 
- Config Key is displayed in Preferences / Exams. If settings are generated server-side, you don't need to copy any hash from SEB to the exam settings, as the hash can be calculated also server-side.
- Now blocking Predictive Text in TouchBar during an exam.
- Improved logging when starting SEB: Now starting to log (with log level Debug and at standard log file path) regardless of current settings directly after SEB starts up, before local persistent settings are initialized.
- Again fixed a bug when SEB could kill itself when a space switch occurred, this time correctly.
- Fixed opening seb(s):// link wasn't working when temporary browser window (for authentication) was open and SEB was restarted after editing preferences.
- Added one point to menu bar height to keep a black edge between menu bar and browser window.
- Fixed a compatibility issue which caused SEB 2.1.2 to crash immediately when started on OS X 10.7.