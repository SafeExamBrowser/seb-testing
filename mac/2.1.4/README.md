**SEB 2.1.4 for macOS Preview Version**

Here you can find the current preview build of the next release of SEB for macOS. A preview version doesn't contain the full functionality of the final release yet, but specific new features and fixes for issues of the current stable release. 

You can support us by testing the pre-release version and give feedback in our forum or by creating an issue here on our GitHub page. 


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