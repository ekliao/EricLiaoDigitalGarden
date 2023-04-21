---
{"dg-publish":true,"permalink":"/programming/asdf-version-manager/","created":"","updated":""}
---

#project/learn-by-doing 

#source/dupe/begin 
[src](https://mac.install.guide/ruby/5.html)
## Install Asdf Version Manager

Most developers will need to install newer Ruby versions as they are released. And they will maintain applications that use older Ruby versions. A version manager makes it easy to switch between Ruby versions.

For a version manager, I recommend [asdf](https://asdf-vm.com/). Asdf can manage versions of many languages, including Ruby and Node. If you don't need support for multiple languages (you are just using Ruby), see instructions for installing [frum](https://mac.install.guide/ruby/14.html) or [chruby](https://mac.install.guide/ruby/12.html).

Here are instructions for installing asdf. You can also check the [asdf installation instructions](https://asdf-vm.com/#/core-manage-asdf) on the asdf website. Older instructions say you should manually install the coreutils dependencies with Homebrew but I've found that all dependencies are automatically installed by the Homebrew asdf script (the Homebrew "formula").

### Install asdf

You can install asdf using Homebrew.

```
$ brew install asdf
```

You can confirm that Homebrew installed asdf with `brew list`.

```
$ brew list
==> Formulae
asdf		ca-certificates	libtool		openssl@1.1
autoconf	coreutils	libyaml		readline
automake	gmp		m4		unixodbc
```

==Success.== After installing asdf with Homebrew, you can view the installed dependencies with `brew deps --tree --installed`.

### Add asdf to the .zshrc file

We must add asdf to the shell environment before we can use it to manage Ruby versions. The Homebrew post-installation message (on Apple Silicon) for asdf says:

```
To use asdf, add the following line to your ~/.zshrc:
. /opt/homebrew/opt/asdf/libexec/asdf.sh
```

The Homebrew post-installation message for asdf also says, "zsh completions have been installed to: /opt/homebrew/share/zsh/site-functions" (on Apple Silicon), meaning that asdf commands are auto-completed by pressing the tab key when you are using the terminal application.

Use a shortcut to configure your shell to use asdf:

```
$ echo -e "\n. $(brew --prefix asdf)/libexec/asdf.sh" >> ~/.zshrc
```

Check the `~/.zshrc` file.

```bash
$ cat ~/.zshrc
```

You should see configuration commands for asdf on the last line. For Mac Intel:

```bash
. /usr/local/opt/asdf/asdf.sh
```

==For me, it is:
`. /usr/local/opt/asdf/libexec/asdf.sh`==
On Apple Silicon:

```bash
. /opt/homebrew/opt/asdf/asdf.sh
```

==Configuration for asdf should always be the last line in the `~/.zshrc` file==, after setting any `$PATH` configuration.

🚩 Close and reopen the Terminal window for the changes to the `~/.zshrc` file to be recognized.

After closing and reopening the Terminal window, use `asdf --version` to check that asdf was installed successfully.

```bash
$ asdf --version
v0.9.0
```

==Mine: 0.11.3== If the asdf command doesn't work, make sure you've added the asdf configuration to your `.zshrc` file and restarted the terminal application.

You can also check that asdf appears in your `$PATH` configuration (this is the Apple Silicon version where Homebrew installs packages in `/opt/homebrew/`):

```bash
$ echo $PATH
/Users/daniel/.asdf/shims:/opt/homebrew/opt/asdf/libexec/bin:/opt/homebrew/bin:/opt/homebrew/sbin:/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin
```

### Add the .asdfrc configuration file

If you are working on any older projects that use a `.ruby-version` file to specify a Ruby version, add a `.asdfrc` configuration file to your user home directory to enable asdf to read `.ruby-version` files.

```bash
$ echo "legacy_version_file = yes" >> ~/.asdfrc
```

Confirm the creation of the configuration file.

```
$ cat ~/.asdfrc
legacy_version_file = yes
```

### Asdf `.tool-versions` file

When you work on a project, you can tell asdf which language versions you need by adding a `.tool-versions` file to your project folder. This is a multi-language alternative to configuration with the `.ruby-version` file.

```
ruby 3.1.0
nodejs 10.16.0
```

### More

The [Uninstall Asdf](https://mac.install.guide/faq/uninstall-asdf/index.html) page explains how to remove asdf, if you decide not to use it.

Next you can install [[programming/Ruby\|Ruby]].

#source/dupe/end 

Next: [[programming/Ruby\|Ruby]]