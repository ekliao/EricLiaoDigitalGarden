---
{"dg-publish":true,"permalink":"/git/","noteIcon":"2","created":"","updated":""}
---

#project/learn-by-doing 

#source/dupe/begin 
[src](https://mac.install.guide/ruby/4.html)
## Configure Git on Mac

[Git](http://git-scm.com/) is automatically installed as part of the Xcode Command Line Tools. It is essential software for save-as-you-go control of the code you write.

Before installing Ruby, you should configure Git. Using [GitHub](https://github.com/) or a similar service, developers collaborate with others and deploy applications for hosting. As a Ruby developer, you'll use Git with a GitHub account for remote backup and collaboration.

Before you configure Git, you should [create an account on GitHub](https://help.github.com/articles/signing-up-for-a-new-github-account/) (it's free). It is important to use the same email address for GitHub and your Git configuration.

Check that Git is installed:

```
$ git version
```

You should see git version 2.30.1 (or newer). ==Mine is 2.32.==

### How to edit Git config file

Configure Git if you haven't used it before. First, list the current settings with the `git config -l --global` command.

```
$ git config -l --global
fatal: unable to read config file '/Users/.../.gitconfig': No such file or directory
```

If you haven't set up Git previously, you'll see "fatal: unable to read config file." Here's how to edit the Git config file.

Set your name and email address (use your real name and the same email address as your GitHub account). Don't just copy and paste the code you see here, use your own name and email.

```
$ git config --global user.name "Eric Liao"
$ git config --global user.email ekliao@gmail.com
```

Check your Git configuration:

```
$ git config -l --global
user.name=Eric Liao
user.email=ekliao@gmail.com
```

![](https://mac.install.guide/assets/images/ruby/configure-git.png)

### Set up password-less login

After you create an account on GitHub, [set up an SSH key](https://help.github.com/articles/connecting-to-github-with-ssh/) so you don't have to enter a username and password every time you connect to GitHub from the Terminal.

```
$ ssh-keygen -t ed25519 -C "ekliao@gmail.com"
Generating public/private ed25519 key pair.
Enter file in which to save the key (/Users/me/.ssh/id_ed25519):
Created directory '/Users/me/.ssh'.
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /Users/me/.ssh/id_ed25519.
Your public key has been saved in /Users/me/.ssh/id_ed25519.pub.
The key fingerprint is:
SHA256:R+t5PZM+g/3f7t/u3ZtGxpcbj1Mmmpcv1mK5Sa5OC8A me@example.com
The key's randomart image is:
+--[ED25519 256]--+
|                 |
|                 |
|          .      |
|       . . .     |
|        E o   . .|
|         + . ..B+|
|          + o=OO=|
|           ++=#*O|
|           .+=*^^|
+----[SHA256]-----+
```

The `ssh-keygen` command creates an encrypted key. You'll be prompted for a file in which to save the key. Press enter for the default.

You'll be prompted for a passphrase to enter whenever you use the encrypted key. You can enter RETURN for no passphrase. This is safe if you are sure only you can log into your Mac user account and access the terminal. If someone else can use your terminal, they can push code to GitHub projects that require your credentials. My advice: Enter a passphrase if you are likely to leave your computer unattended and your account logged in. Otherwise, save yourself extra effort and leave the passphrase empty if you're the only one who can use your account to push code to GitHub.

You'll need to enter the public key (NOT the private key) to set up password-less login on your GitHub account.

Use a shortcut to copy the public key to your macOS clipboard:

```
$ pbcopy < ~/.ssh/id_ed25519.pub
```

Or you can display the public key with the `cat ~/.ssh/id_ed25519.pub` command and copy and paste it.

Copy the public key from the Terminal and [paste it here](https://github.com/settings/ssh) in your GitHub settings. ==It worked!==

Verify the SSH key is configured correctly:

```
$ ssh -T git@github.com
The authenticity of host 'github.com (52.74.223.119)' can't be established.
RSA key fingerprint is SHA256:nThbg6kXUpJWGl7E1IGOCspRomTxdCARLviKw6E5SY8.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
```

After answering "yes" to continue, you should see:

```
Warning: Permanently added 'github.com,52.74.223.119' (RSA) to the list of known hosts.
Hi (name)! You've successfully authenticated, but GitHub does not provide shell access.
```

==Same for me!== Now you'll be ready to use GitHub when you need it. ==Oh yay!== Unless you've encountered a connection problem.

### Troubleshooting connection problems

Some Internet service providers (ISPs) block connections on port 22. Your ISP may be blocking port 22 if you get error messages like this:

```
$ ssh -T git@github.com
ssh: connect to host github.com port 22: Connection refused
$ ssh -T git@github.com
ssh: connect to host github.com port 22: Network is unreachable
```

It's difficult to see that the problem lies with your ISP and not your computer or GitHub. You can connect on port 443 instead. Try the workaround.

Create a file `~/.ssh/config` and add a setting so connections to GitHub will use port 443.

```bash
$ touch ~/.ssh/config
```

Edit the file to add:

```
Host github.com
  Hostname ssh.github.com
  Port 443
```

After saving the ssh configuration file, try connecting to GitHub with `ssh`:

```
$ ssh -T git@github.com
The authenticity of host '[ssh.github.com]:443 ([192.30.255.122]:443)' can't be established.
RSA key fingerprint is SHA256:nThbg6kXUpJWGl7E1IGOCspRomTxdCARLviKw6E5SY8.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[ssh.github.com]:443,[192.30.255.122]:443' (RSA) to the list of known hosts.
Hi DanielKehoe! You've successfully authenticated, but GitHub does not provide shell access.
```

Now you'll be ready to use [[programming/GitHub\|GitHub]] when you need it.

#source/dupe/end 

Next is installing the [[Asdf Version Manager\|Asdf Version Manager]]