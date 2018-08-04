**SEB 2.1.4 for macOS Preview Version**

Here you can find the current preview build of the next release of SEB for macOS. A preview version doesn't contain the full functionality of the final release yet, but specific new features and fixes for issues of the current stable release. 

You can support us by testing the pre-release version and give feedback in our forum or by creating an issue here on our GitHub page. 


New in SEB 2.1.4pre1 for macOS (29ED):
- SEBMAC-146 Fixed: JavaScript confirm dialog doesn't return false when cancel button is clicked (see https://github.com/SafeExamBrowser/seb-mac/issues/24, thanks for reporting the issue, pkarjala)
- SEBMAC-145 Fixed opening a seb(s) link from another browser which requires authentication while SEB is running subsequently can fail:
When the temporary browser window for authentication is closed (windows close button), then SEB ignores further external (as from the other browser) open seb(s) URL calls.