# Default Screen Location

By default, OSX saves all of your screenshots to your desktop. If you want screenshots to be saved in another directory, you can run the following commands in Terminal:

```
~$ defaults write com.apple.screencapture location <directory>
~$ killall SystemUIServer
```

where `<directory>` is the directory that you want to save screenshots in.

[source](http://osxdaily.com/2011/01/26/change-the-screenshot-save-file-location-in-mac-os-x/)