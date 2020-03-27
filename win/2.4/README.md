**SEB for Windows 2.4 Preview Version**

Here you can find the current pre-release build of the next release of SEB for Windows. This is a feature-complete beta version, ready for final testing before a public release. You can support us by testing the pre-release version and give feedback in our forum or by creating an issue here on our GitHub page.

New in SEB 2.4pre1 for Windows: 
- Config Key feature, hash checksum value to verify settings used by SEB. The Config Key can be generated automatically by a compatible exam system together with the SEB config to be used for an exam. All SEB versions supporting the Config Key generate the same key, as long as the same SEB config file is used. 
- Implemented setting keys to control clearing cookies when starting/ending a session (examSessionClearCookiesOnStart / examSessionClearCookiesOnEnd). This can be used to keep users logged in (SEB started with client settings) after an exam session was started.
- Now TLS 1.2 is supported for downloading .seb files using sebs:// links.
- Private clipboard should now also work correctly with rich-text editors like TinyMCE (fixed double pasting of text). 
- Fixed two minor issues regarding port and path filtering in URL filter.
- Fixed wrong error message in case service fails to set registry values.
- Fixed an index out of range exception when starting additional resource with application.
