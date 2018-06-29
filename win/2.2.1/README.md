**SEB for Windows 2.2.1 Preview Version**

Here you can find the current pre-release build of the next release of SEB for Windows. You can support us by testing the pre-release version and give feedback in our forum or by creating an issue here on our GitHub page.

New in SEB 2.2.1pre7 for Windows:
- Prevent that SEB browser can be used to finish an exam if SafeExamBrowser.exe is terminated: Added updated seb2 browser app with lock screen implementation.
- Replaced embedded Firefox with latest version 52.9.0 ESR.
- Changed default setting for all function keys to "enabled".
- Only show additional resource button if it is active.

New in SEB 2.2.1pre6 for Windows:
- Removed "Interop.WUApiLib.dll" binary no longer in use from creation of Browser Exam Key BEK and added new binaries.
- Changed ProcessWatchDog to distinguish processes by ID in order to detect new instances of Firefox (not seb2) being started.

New in SEB 2.2.1pre5 for Windows:
- Fixed bug which deleted files from the temporary additional resources folder.
- Fixed Additional Resources option "Show confirm box" not working.
- Fixed PDF response observer to ignore frame requests.
- Updated browser engine to latest version.
- Changed wording of client configuration message.
- Removed key KeyAdditionalResourcesIdentiﬁerCounter, which isn't acutally used and in addition caused a problem because it was using a strange joint "fi" unicode character.

New in SEB 2.2.1pre4 for Windows:

- Fixed bug in reconfiguration mechanism which caused unnecessary reconfiguration during startup.
- Fixed bug not hiding additional resource details when deleting last resource.
- Extended SID handling to always try all available methods to retrieve a SID.
- Fixed major bug which could lead to an invalid SID value being saved in the registry backup file.

New in SEB 2.2.1pre3 for Windows:

- Attempt to resolve concurrency issue in web socket communication with browser.
- Fixed deadlocks and multi-threading issues when starting SEB with a Quit-URL.
- Fixed bug trying to kill the System Idle Process when an allowed application (Firefox) was running during startup in Create New Desktop mode.
- Extended message about remote desktop connections in registry resetter.
- Updated InstallShield installer to always perform a major update and disabled small/minor updates.

New in SEB 2.2.1pre2 for Windows:

- Improved logging and functionality of Registry Resetter
- Now expanding environment variables in process arguments
- Second attempt to fix that Browser Exam Key (BEK) check wasn't working correctly with some exam systems (because a trailing slash "/" was removed from the URL used to hash the BEK)
- Fixed: If blocked URL is opened as a new window, the message "calling this URL is not allowed" is displayed behind a white page
- Fixed: If canceling opening a seb(s):// link (inside SEB), the SEB browser tries to download the config file
- Fixed: Quit Link option "Ask user to confirm quitting" not working in some cases

New in SEB 2.2.1pre1 for Windows:

- Added configurable spell checking, dictionaries can be embedded into SEB config files. 
- Added context menu for displaying word suggestions and selecting spell checking dictionary. Note: You have to enable the right mouse button in "Hooked Keys" config tool tab. 

Added options for additional resources: 
- Show button (to display the icon or menu entry for a resource)
- Referrer filter for activation Link URL
- Option "Show confirm box" with custom text which is displayed before loading a resource
- Reset browser session (session cookies are deleted before loading a new resource)

- Fixed that SEB couldn't quit Firefox when starting. In SEB 2.2, as a workaround you can explicitly add Firefox as prohibited process with the option "Force quit" activated. But warn your students that a running Firefox will be force terminated and they might loose entered text or open tabs
- Fixed Desktop wallpaper wasn't restored sometimes after quitting SEB
- Fixed Ctrl+1/2/3/.../9 allowed changing "tabs", which could lead to users getting stuck on a white page if they pressed the key combination unwittingly
- Fixed changed browser user agent wasn't updated correctly
- Fixed that the URL filter didn't treat query strings in URLs consistently in SEB for Windows 2.2/macOS. Added option to explicitly forbid any query part in checked URL: Indicate "?." as query in your filter expression.
- Fixed Basic Authentication login wasn't working
- Now always removing trailing slash from Quit URL before comparing it with current URL
- Fixed SEB trying to close Firefox when opening a .seb file while SEB is already running
- Fixed URL filters weren't saved for exam mode configs
- Fixed reconfiguring from touch optimized to "desktop" mode: Taskbar stayed large
- Fixed .seb config file as additional resource wasn't loaded by SEB