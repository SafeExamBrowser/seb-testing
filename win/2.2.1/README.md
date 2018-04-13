**SEB for Windows 2.2.1 Preview Version**

Here you can find the current pre-release build of the next release of SEB for Windows. You can support us by testing the pre-release version and give feedback in our forum or by creating an issue here on our GitHub page. 

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
- Fixed that Browser Exam Key (BEK) check wasn't working correctly with some exam systems (because a trailing slash "/" was removed from the URL used to hash the BEK)
- Fixed changed browser user agent wasn't updated correctly
- Fixed that the URL filter didn't treat query strings in URLs consistently in SEB for Windows 2.2/macOS. Added option to explicitly forbid any query part in checked URL: Indicate "?." as query in your filter expression.
- Fixed Basic Authentication login wasn't working
- Now always removing trailing slash from Quit URL before comparing it with current URL
- Fixed SEB trying to close Firefox when opening a .seb file while SEB is already running
- Fixed URL filters weren't saved for exam mode configs
- Fixed reconfiguring from touch optimized to "desktop" mode: Taskbar stayed large
- Fixed .seb config file as additional resource wasn't loaded by SEB

Known issues in this build:
- If blocked URL is opened as a new window, the message "calling this URL is not allowed" is displayed behind a white page
- If canceling opening a seb(s):// link (inside SEB), the SEB browser tries to download the config file