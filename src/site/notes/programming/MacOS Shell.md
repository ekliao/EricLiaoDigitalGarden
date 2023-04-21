---
{"dg-publish":true,"permalink":"/programming/mac-os-shell/","created":"","updated":""}
---

#project/learn-by-doing 

#source/dupe/begin 
[src](https://mac.install.guide/ruby/1.html)
- Show/hide (toggle) hidden files (those beginning with a dot):
	- You can list all files, including hidden files, with the `ls -lag` command in the Terminal.
	- In the macOS Finder (the file browser), you can enter Command + Shift + . to show hidden files. If you want to hide those files again, you can enter the same keystrokes.
	- You can force the Mac to always display hidden files by entering the following command in the Terminal application (Hidden files will appear in gray in the Finder window.):
```bash
$ defaults write com.apple.finder AppleShowAllFiles TRUE; killall Finder
```

#source/dupe/end 

Next: [[programming/Xcode\|Xcode]]

# [[programming/Ruby\|Ruby]]
# [[programming/Git\|Git]]

