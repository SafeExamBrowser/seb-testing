**SEB 2.1.4 for macOS Preview Version**

Here you can find the current preview build of the next release of SEB for macOS. A preview version doesn't contain the full functionality of the final release yet, but specific new features and fixes for issues of the current stable release. 

You can support us by testing the pre-release version and give feedback in our forum or by creating an issue here on our GitHub page. 


New in SEB 2.1.4 (Release Candidate 2) for macOS (2B62):
- SEBMAC-93 Fixed modal lock when webpage tries to download a font
by sending a return event tap to close the Font Download dialog: Made this work more reliably by waiting one second before sending return key event tap. Fixed issue under Catalina when creating the CGEventCreateKeyboardEvent on the main thread.
- SEBMAC-93 To prevent a modal lock when webpage tries to download a font and SEB doesn't have Accessibility permissions, before terminating SEB, save information that this happened and on which web page it happened (title and URL or placeholder). This will be displayed when SEB is started next time.
- SEBMAC-93 Made sure check for Accessibility permission isn't accessed on macOS < 10.9 (API available on macOS >= 10.9). 
- SEBMAC-202 Fixed: Alert for not being able to restore the "Touch Bar shows App Controls" mode was sometimes not displayed (especially under Catalina), probably when the terminated Touch Bar process wasn't restarted yet.



New in SEB 2.1.4 (Release Candidate) for macOS (2B12):
- Set default minimal macOS version to 10.11.


New in SEB 2.1.4pre6 for macOS (2B0D):
- SEBMAC-204 Fix opening of SEB config files/links wasn't working anymore (regression).
- SEBMAC-189 Selecting multiple files for upload is now controlled by the HTML input element (multiple-attribute).
- SEBMAC-210 SEB Dock button disappearing on macOS 10.10 - 10.13 instead of being highlighted when right/long clicked.
- SEBMAC-93 Fixed modal lock when webpage tries to download a font and SEB doesn't have the Privacy / Accessibility right to send a return event tap to close the Font Download dialog: Checking if SEB is allowed to use Accessibility only when running on macOS 10.9 or newer.
- Fixed layout constraints in Exam prefs pane.
- Updated German localization.


New in SEB 2.1.4pre5 for macOS (2AED):
- SEBMAC-158 Fixed calculating Config Key hash (updated code with current iOS version's).
- SEBMAC-216 Set default minimal macOS version to 10.12.
- SEBMAC-204 Fixed downloading and opening of SEB config files defined on website as data: was possible even when an exam session was already running.
- SEBMAC-210 Fixed background of Dock buttons when clicked wasn't working anymore on macOS < 10.14.
- SEBMAC-205 Fixed Preferences / Exams showed instead of Browser Exam and Config Keys that the SEB config (loaded with seb(s) link) was modified.
- SEBMAC-213 Removed using or sending global hotkeys, except in the case the Font Download dialog is displayed.
- SEBMAC-93 Fixed modal lock when webpage tries to download a font and SEB doesn't have the Privacy / Accessibility right to send a return event tap to close the Font Download dialog: Now SEB is terminated in this case.
- SEBMAC-213 Removed global hotkeys for F3+F6 shortcut to open Preferences window (F3+F6 shortcut now only works if SEB is the active application).
- SEBMAC-204 Fix downloading and opening of SEB config files defined on website as data still didn't work if the HTTP response wasn't containing the full filename including ".seb".
- SEBMAC-202 Show error for not being able to disable custom Quick Actions in Touch Bar only when there actually is a Touch Bar.
- SEBMAC-188 Fixed issue with NSHomeDirectory() not correctly working on macOS Mojave (always returning sandboxed home directory location even though the app isn't sandboxed!).
- SEBMAC-198 Fixed checking for agent processes.


New in SEB 2.1.4pre4 for macOS (2AC9):
- SEBMAC-186 Implemented key shortcuts for switching between open browser windows.
Left Alt (Option) Key +Tab: Cycle forward through open browser windows
Left Alt (Option) Key + Left Shift Key + Tab: Cycle backwards through open browser windows
Right Alt (Option) Key (+ Right Shift) + Tab keeps the standard function (cycle through website elements).
- SEBMAC-202 Custom App Controls and Quick Actions in Touch Bar with Control Strip active are now disabled, even if BetterTouchTool is used.
Added alert when App Control mode for Touch Bar couldn't be restored automatically, offering to open System Preferences / Keyboards so user can change the setting back manually.
- SEBMAC-189 Now selecting multiple files for upload is possible.
- SEBMAC-179 Import identity with exportable private key when opening it in the Preferences window. Now displaying error when an identity couldn't be exported from the Keychain.
- SEBMAC-210 Fixed: Background of Dock buttons is highlighted when clicked and button is white instead of gray.
- SEBMAC-203 Don't display SIGSTOP lock screen when Mac is set to sleep mode. Improved SIGSTOP detection in case system time is changed. Background of lock screen log view is again white also on Mojave.
- SEBMAC-204 Fixed downloading and opening of SEB config files defined on website as data: didn't work. Also there was an issue with the default ~/Downloads directory when running on Mojave.


New in SEB 2.1.4pre3 for macOS (2A61):
- SEBMAC-198 Implemented blocking macOS screen recording (cmd+shift+5) introduced in Mojave, controlled with setting Preferences / Security / Allow screen capture (key enablePrintScreen).
- SEBMAC-202 Now disabling custom Quick Actions in Touch Bar.	
- SEBMAC-200 Fixed: Starting SEB with seb(s) link doesn't open config from that URL on some systems.
- SEBMAC-193 Fixed: Media player app can block SEB with play button. The previous implementation didn't work properly on Mojave.
- SEBMAC-188 Fixed downloads not working in macOS 10.14 Mojave.
- SEBMAC-187 SEB application is now notarized and uses the Hardened Runtime feature.


New in SEB 2.1.4pre2 for macOS (29FA):
- SEBMAC-158 Fixed calculating Config Key hash by removing empty salt value (as we're not using a salt with Config Key). Now a standard sha256 calculation of the config key json string produces the same hash as SEB calculates and displays in the Preferences/Exam pane.
- SEBMAC-160 When checking server trust with embedded certificates, resources in subdomains of already trusted domains are now trusted as well, according to behavior in other standard browsers.
- Added delegate method which returns a placeholder text in case settings don't allow to display its URL.


New in SEB 2.1.4pre1 for macOS (29ED):
- SEBMAC-146 Fixed: JavaScript confirm dialog doesn't return false when cancel button is clicked (see https://github.com/SafeExamBrowser/seb-mac/issues/24, thanks for reporting the issue, pkarjala)
- SEBMAC-145 Fixed opening a seb(s) link from another browser which requires authentication while SEB is running subsequently can fail:
When the temporary browser window for authentication is closed (windows close button), then SEB ignores further external (as from the other browser) open seb(s) URL calls.