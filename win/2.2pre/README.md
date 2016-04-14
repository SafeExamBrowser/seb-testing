*SEB 2.2 Preview Version*

Here you can find the current preview build of the next major release of SEB for Windows. Preview builds don't include all the functionality of the final version, they are not tested thoroughly and they are not intended for productive use. You can support us by testing the preview version and give feedback in our forum or by creating an issue here on our GitHub page. 

New in SEB 2.2:
- Replaced the deprecated Mozilla XULRunner browser engine by a full Firefox browser (which is nevertheless running in the same mode with reduced functionality).
- Refactored seb2 XUL browser app.
- Support for additional resources, which can be external (defined by a URL) or embedded into the SEB config file. An embedded resource can be one file or a whole directory with subdirectories, which can either be opened and displayed by the SEB browser or one of the permitted applications.
- SEB can load one of the embedded resources instead of an URL. With this feaure pure offline exams can be done if using a offline exam player.

Known limitations:
- This preview version does not yet automatically add URL filter rules when an external additional resource is added. Activate URL filtering and create filter rules manually. 

This document is subject to change, if you're testing SEB 2.2, please check out this document regularly.
