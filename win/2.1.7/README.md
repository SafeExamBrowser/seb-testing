**SEB 2.1.7 Testing Version**

Here you can find the current pre-release build of the next maintenance update of SEB for Windows. You can support us by testing the pre-release version and give feedback in our forum or by creating an issue here on our GitHub page. 

New in SEB 2.1.7:

- Improved detecting permitted and prohibited processes. 
- Added new settings sub-key originalName to permitted and prohibited processes.
- Extensions are now stripped from executable and original filenames before comparing to running processes.
- Fixed error when displaying which running processes must be terminated before starting exam.
- Now adding list of prohibited (browser) processes automatically to all config files which SEB Client or SEB Config Tool opens, unless a prohibited process with the same name already exists. If you need to allow one of these processes, then just deselect the "Active" flag of that process in the list of prohibited processes.
- Automatically disabling Chrome notifications using a Registry setting.