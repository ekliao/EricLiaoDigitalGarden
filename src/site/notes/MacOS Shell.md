---
{"dg-publish":true,"permalink":"/mac-os-shell/","noteIcon":"2","created":"","updated":""}
---

This is the beginning of a series of pages that I followed to set up my MacOS development environment in preparation for publishing my Obsidian vault. It seems daunting at first but turned out not that difficult because of the excellent guide by  [Daniel Kehoe](https://twitter.com/yaxdotcom).

#project/learn-by-doing 

#paste/b 
[src](https://mac.install.guide/ruby/1.html)
- Show/hide (toggle) hidden files (those beginning with a dot):
	- You can list all files, including hidden files, with the `ls -lag` command in the Terminal.
	- In the macOS Finder (the file browser), you can enter Command + Shift + . to show hidden files. If you want to hide those files again, you can enter the same keystrokes.
	- You can force the Mac to always display hidden files by entering the following command in the Terminal application (Hidden files will appear in gray in the Finder window.):
```bash
$ defaults write com.apple.finder AppleShowAllFiles TRUE; killall Finder
```

#paste/e 

Next: [[Xcode\|Xcode]]

# [[Ruby\|Ruby]]
# [[Git\|Git]]

