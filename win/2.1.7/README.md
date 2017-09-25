**SEB 2.1.7 Testing Version**

Here you can find the current pre-release build of the next maintenance update of SEB for Windows. You can support us by testing the pre-release version and give feedback in our forum or by creating an issue here on our GitHub page. 

New in SEB 2.1.7:

- Fixed bugs in improvements from previous build.
- Fixed using alt-tab switching between several browser windows displays two bars.
- Back ported bugfix for from SEB 2.2 to 2.1.7.
- Fixed autostart error when using SEB 2.2 generated settings with SEB 2.1.7. If permitted process firefox.exe for SEB browser was contained in settings (because those were created in SEB 2.2), the permitted process following SEB/firefox.exe in the list of permitted processes was autostarted, even if that flag wasn’t set.
- Improved detecting permitted and prohibited processes. 
- Added new settings sub-key originalName to permitted and prohibited processes.
- Extensions are now stripped from executable and original filenames before comparing to running processes.
- Fixed error when displaying which running processes must be terminated before starting exam.
- Now adding list of prohibited (browser) processes automatically to all config files which SEB Client or SEB Config Tool opens, unless a prohibited process with the same name already exists. If you need to allow one of these processes, then just deselect the "Active" flag of that process in the list of prohibited processes.
- Automatically disabling Chrome notifications using a Registry setting.