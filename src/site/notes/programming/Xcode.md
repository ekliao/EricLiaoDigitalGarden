---
{"dg-publish":true,"permalink":"/programming/xcode/","created":"","updated":""}
---

#project/learn-by-doing 

#source/dupe/begin 
[src](https://mac.install.guide/ruby/2.html)
## Xcode Command Line Tools

You need to install Apple's Xcode Command Line Tools to get the Unix tools needed to install Ruby and develop applications. Apple’s Xcode Command Line Tools provide a C language compiler. You'll need it to install Ruby. Also, for many Ruby projects, you will need the C language compiler to automatically install gems that use native extensions (some gems speed up Ruby by using code written in C).

Xcode is Apple's software library for macOS developers. Xcode is over 40GB. You don't need all of it!. You just need the Xcode Command Line Tools. Only install the full 40GB Xcode package if you plan on doing development of applications for the Apple operating systems (macOS or iOS apps). Here you’ll learn how to just install the Command Line Tools that give you common Unix utilities.

It's easiest to install Command Line Tools as a part of installing Homebrew, the Unix utilities package manager. **If you have a fresh install of macOS, skip ahead to the next section,** [Install Homebrew](https://mac.install.guide/ruby/3.html).

If you updated your macOS from an earlier version, you may have an outdated version of Xcode. Read on to check if you have a troublesome out-of-date Command Line Tools.

### Is Xcode already installed?

If you updated your macOS from an earlier version (sometimes called an "over the top" installation), and you previously installed a Ruby development environment, your earlier installation remains intact. You will need to install the new version of Xcode Command Line Tools to avoid headaches. First, check what you have.

Check if you previously installed the full Xcode package:

```bash
$ xcode-select -p
```

#### Scenario 1

If you see, `xcode-select: error: unable to get active developer directory...`, the Xcode package is not installed.

Good! Jump to the section, [Install Homebrew](https://mac.install.guide/ruby/3.html).

![](https://mac.install.guide/assets/images/ruby/xcode-not-installed.png)_The Xcode package is not installed_

#### Scenario 2

If you see a file location that contains spaces in the path:

```bash
/Applications/Apple Dev Tools/Xcode.app/Contents/Developer
```

you will have problems installing Ruby. You should delete Xcode before continuing.

#### Scenario 3

If you see:

```bash
/Applications/Xcode.app/Contents/Developer
```

The full Xcode package is already installed. ==This is the case for me!== Perhaps you installed it previously. If Xcode is installed, you will need to update Xcode to the newest version (Xcode 13.2 or newer). **Go to the App Store application and check "Updates."** After updating Xcode, be sure to launch the Xcode application and accept the Apple license terms.

#### Scenario 4

If you see:

```bash
/Library/Developer/CommandLineTools
```

The Xcode Command Line Tools may be installed or an empty directory may be present.

Here's how to test:

```bash
$ ls /Library/Developer/CommandLineTools/usr/bin/git
```

You should see:

```bash
/Library/Developer/CommandLineTools/usr/bin/git
```

Check that you can run `git`:

```bash
$ git --version
git version 2.30.1 (Apple Git-130)
```

> I can! My Git version is 2.32.

If Xcode Command Line Tools are installed, you can skip ahead to install [[programming/Homebrew\|Homebrew]].

If the Xcode Command Line Tools folder is empty, you should remove it.

Remove the empty folder:

```bash
$ sudo rm -rf /Library/Developer/CommandLineTools
```

You are using sudo for admin privileges so you must enter the password you use to log in to your computer (you will not see the password after entering it). After removing the folder, continue to the section, "Install Homebrew."

#source/dupe/end 

Next: [[programming/Homebrew\|Homebrew]]