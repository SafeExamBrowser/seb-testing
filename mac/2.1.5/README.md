**SEB 2.1.5 for macOS Preview Version**

Here you can find the current preview build of the next release of SEB for macOS. A preview version doesn't contain the full functionality of the final release yet, but specific new features and fixes for issues of the current stable release. 

You can support us by testing the pre-release version and give feedback in our forum or by creating an issue here on our GitHub page. 


New in SEB 2.1.5pre1 for macOS (2B82):

- SEBMAC-221 Fixed: Wrong Config Key is calculated when new SEB version adds new default settings which is a dictionary/array.
- SEBMAC-223 Removed ARDAgent from detecting Remote Management:
ARDAgent is running always when Remote Management is enabled in System Preferences / Sharing. It should be enough to detect the processes ScreensharingAgent and AppleVNCServer (Back to My Mac on macOS < 10.14 Mojave).
- SEBMAC-222 Fixed: Client config encrypted with password isn't compatible between Win vs. Mac+iOS.
Problem with uppercase/lowercase password hashes, solved by encrypting with lowercase hash (like in Windows version) and decrypting by both lowercase (for client config saved in Win and macOS 2.1.15+ version) and lowercase (macOS version < 2.1.5).