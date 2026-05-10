---
{"dg-publish":true,"permalink":"/ruby/","noteIcon":"2","dg-note-properties":{}}
---

#project/learn-by-doing 

Here's an amazingly helpful, hand-holding [guide](https://mac.install.guide/ruby/index.html) to installing Ruby by Daniel Kehoe. This is the prerequisite for embarking on a journey of [[GitHub\|GitHub]] and static web hosting (for free) using [[Hugo\|Hugo]]. So, get with it.

#paste/b 
[src](https://mac.install.guide/ruby/6.html)
## Install Ruby with Asdf

Here are instructions for installing Ruby using asdf, the software version manager. If you are not using asdf, you can see instructions to [Install Ruby with frum](https://mac.install.guide/ruby/14.html) or [Install Ruby with Homebrew](https://mac.install.guide/ruby/13.html).

If you plan to use asdf, be sure you've completed the section, [Install Asdf Version Manager](https://mac.install.guide/ruby/5.html).

### Mac system Ruby

MacOS comes with a "system Ruby" pre-installed. MacOS Monterey includes Ruby 2.6.8 which is not the newest version. ==Mine is 2.6.10p210.== ==*It's a bad idea to use the Mac system Ruby.*== See the article [Do not use the MacOS system Ruby](https://mac.install.guide/faq/do-not-use-mac-system-ruby/index.html). You can see the system Ruby with `which ruby` and `ruby -v`.

![](https://mac.install.guide/assets/images/ruby/macos-system-ruby.png)

Leave the system Ruby in place and use the software version manager to install the newest Ruby version.

### Install Ruby with Asdf

Check online for the current [recommended version of Ruby](http://www.ruby-lang.org/en/downloads/).

When this was written, Ruby 3.1.0 was the newest version (3.1.0 was released on Dec 25, 2021). ==Now: 3.2.2.==

First, install the asdf plugin for Ruby:

```
$ asdf plugin add ruby
```

See all the versions of Ruby that are available:

```
$ asdf list all ruby
```

If you don't see the newest version of Ruby, update the asdf plugin for Ruby and try again:

```
$ asdf plugin-update ruby
$ asdf list all ruby
```

Install the latest version of Ruby:

```
$ asdf install ruby latest
```

==This installs 3.2.2 for me.== You’ll see diagnostic messages and progress updates. Installation takes less than five minutes on Apple Silicon with a fast Internet connection.

Asdf automatically installs OpenSSL which is a dependency for many Ruby gems.

You need to specify a default version of Ruby in your home `~/.tool-versions` file. You can set the `~/.tool-versions` file with a command:

```
$ asdf global ruby 3.1.0
```

🚩 After installation, ==close and re-open the terminal window.==

### Verify installation of Ruby

Verify that the newest version of Ruby is installed with `ruby -v`.

![](https://mac.install.guide/assets/images/ruby/verify-ruby-install.png)

==I see 3.2.2. Yay!== When this was written, Ruby 3.1.0 was the newest version (3.1.0 was released on Dec 25, 2021).

If you see Ruby version 2.6.8, it is the system Ruby and you likely forgot to close and re-open the terminal window.

If you see `No version set for command ruby`, you need to specify a default version of Ruby in your asdf `~/.tool-versions` file.

For example, create a `~/.tool-versions` file like this:

```
ruby 3.1.0
```

The [Tips: Uninstalling Ruby](https://mac.install.guide/ruby/9.html) section explains where Ruby versions are installed and how to remove them.

Next, you can optimize the Ruby development environment by updating gems. See the next section, [Update Gems](https://mac.install.guide/ruby/7.html).

### Using asdf as a version manager

You can install an earlier version of Ruby, for example Ruby 2.7.3.

```bash
$ asdf install ruby 2.7.3
```

For the current shell session, you can switch Ruby versions from the command line with `asdf shell ruby 2.7.3`. Opening the terminal will always use the default version of Ruby you specified initially with `asdf global ruby 3.1.0`.

The command `asdf list ruby` will show all installed versions of Ruby.

```bash
$ asdf list ruby
```

To override the default version of Ruby for a particular project, move into the project root directory and enter the command `asdf local ruby <version>`.

```bash
$ asdf local ruby 2.7.3
```

The command will write a file `.tool-versions` file in the current directory containing a Ruby version number.

The command `asdf current` will display all the asdf-installed software versions that are currently active.

If you no longer need a Ruby version, asdf can remove it with `asdf uninstall ruby 2.7.3`.

#paste/e 

Next is updating [[RubyGem\|RubyGem]].