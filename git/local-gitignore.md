Local gitignore
================

Ignore files only for the local system
.git/info/exclude

If you need to add a file to a shared repository but want that file to be ignored
you can create an entry in .git/info/exclude

This works similarly to .gitignore but it will not be shared with the rest of the
repository. This is perfect if you have files that you commonly change and want to
keep a local copy without updating the shared .gitignore

