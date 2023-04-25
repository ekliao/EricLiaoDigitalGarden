---
{"dg-publish":true,"permalink":"/setting-up-quartz-and-hugo-for-publishing-obsidian-vault/","noteIcon":"2","created":"","updated":""}
---

#project/learn-by-doing  
#project/started 

## Goal
Setting up and running a working static web site for my professional Obsidian vault, which I intend to name "Eric Liao Interpreting."

## Results
I was successful in publishing a subset of my Obsidian vault [here](https://ericliaointerpreting.netlify.app)
, but not with Hugo nor Quartz as the rest of this note describes, but with [[Web publishing with Obsidian + Github + Netlify\|Obsidian Digital Garden plugin + Github + Netlify]].

## Steps
1. I successfully followed [[people/Daniel Kehoe\|Daniel Kehoe]]'s excellent [guide](https://mac.install.guide/ruby/index.html) in setting up the [[Ruby\|Ruby]] and [[GitHub\|GitHub]] development environment on my [[MacOS\|MacOS]]. My process started [[MacOS Shell\|here]].
	1. MacOS
	2. Shell
	3. Xcode
	4. Homebrew
	5. Git
	6. asdf
	7. Ruby 3.1
	8. RubyGem
2. Follow [[Brandon Boswell\|Brandon Boswell]]'s [video](https://www.youtube.com/watch?v=ITiiuBNVue0) and [article](https://brandonkboswell.com/blog/Publishing-your-Obsidian-Vault-Online-with-Quartz/) to set up [[Quartz\|Quartz]] and [[Hugo\|Hugo]].

Below, I duplicate Boswell's article so I can follow and comment.

#source/dupe/begin 
[src](https://brandonkboswell.com/blog/Publishing-your-Obsidian-Vault-Online-with-Quartz/)
# PUBLISHING YOUR OBSIDIAN VAULT ONLINE WITH QUARTZ

Written March 23, 2022

> NOTE: The easiest way to publish your vault online is by using [[[Obsidian Publish\|[Obsidian Publish]]](https://obsidian.md/publish). I put a bunch of time into figuring out how all of this would work together, and I probably could have saved a bunch of time by just using [[Obsidian Publish\|Obsidian Publish]]. Either way, I’ve learned a ton in setting this up. I also have more control on what does and doesn’t get published. I have a ton of private content in my vault and I do not want that being published, which is why I went to all this trouble you’re about to see. Yes, I could use multiple vaults, but that seems annoying when you want to link to something that resides in another vault.

So you’re thinking about publishing your [Obsidian](https://brandonkboswell.com/Obsidian/) Vault online, but you’re not sure if you want to pay for _[[Obsidian Publish\|Obsidian Publish]]_ or not. I’ve been there, that was the exact same situation I was in when I considered publishing my vault. Call me cheap, but I wasn’t sure if I was ready to pay $20 a month for the rest of time. Would I keep writing meaningful content, would people actually ready it? So instead, I decided I was going to figure out a way to publish my vault without the monthly fee. I now publish my vault online, and I don’t pay anything for hosting. **(You are currently reading this article from the digital vault that I publish through this method)**

-   For me, I cobbled together a combination of:
    -   [**Quartz**](https://github.com/jackyzha0/quartz)
        -   A nice, clean-looking template for your digital garden that sits on top of _Hugo_. Once you get your bearings with it, you will find that it is just a _Hugo_ site and you can customize it a ton if you would like.
    -   **[Obsidian Export](https://github.com/brandonkboswell/obsidian-export/tree/title_frontmatter)** (Slightly Modified)
        -   A Rust based library for converting your Obsidian Vault to standards compliant _Markdown_ that supports translating Obsidian style links to standard links that are compatible with Hugo.
        -   Quartz and Hugo both assume that all of your files have a title attribute in their frontmatter. Unfortunately, most of my files do not have this title front matter. I have a branch of obsidian-export (linked above) that uses the file’s name to generate titles when that frontmatter is not present.
    -   **[obsidian-hugo](https://github.com/jackyzha0/hugo-obsidian)**
        -   _Quartz_ has an easy setup that allows you to commit all of your content to _[[GitHub\|Github]]_ and it will compile everything via _Github Actions_. This is fantastic and super helpful. The issue is I have private content that I don’t want on Github.
        -   So instead I use the _obsidian-hugo_ library that Quartz’s Github Action uses just I use it on my local machine and precompile the filtered content before uploading to Github. This enables me to host my Digital Garden on Github (for free) without risking private content accidentally leaking out onto the internet.
    -   [**Github Pages**](https://docs.github.com/en/pages/quickstart)
        -   This is where I publish the content that gets output. It’s all static html and is being served by Github. There is no amount of traffic I could ever manage to generate that Github couldn’t handle.


### Why do I use Obsidian Export when Obsidian Hugo is required by Quartz and does most of the same things?

-   **obsidian-export** does a very good job of filtering out files and folders you don’t want exported
-   it makes me confident that there is no chance that private data gets uploaded by not even allowing that data to be in the folder that gets parsed
-   It handles bad or no frontmatter so that the downstream pipeline doesn’t have any issues
-   You can avoid a bunch of hacks to Quartz (and your layout files) by ensuring that your files have title attributes in their frontmatter. I have hacked together a fork of obsidian-export that does this automatically based on the file name when exporting. [https://github.com/brandonkboswell/obsidian-export/tree/title_frontmatter](https://github.com/brandonkboswell/obsidian-export/tree/title_frontmatter)

# High Level Steps (these are from memory as I set this up a few months ago)

1.  Clone [Quartz](https://github.com/jackyzha0/quartz) into a local directory
> under `code` > `https`, I copied the URL and executed this way in command-line, successfully:
```
ekliao@ELI-1T-Side-MBP14 ~ % git clone https://github.com/jackyzha0/quartz.git
Cloning into 'quartz'...

remote: Enumerating objects: 12369, done.

remote: Total 12369 (delta 0), reused 0 (delta 0), pack-reused 12369

Receiving objects: 100% (12369/12369), 8.56 MiB | 3.04 MiB/s, done.

Resolving deltas: 100% (6105/6105), done.

ekliao@ELI-1T-Side-MBP14 ~ %
```

2.  Create a Repo on Github to host your public garden
    1.  [Getting started with Github Pages](https://levelup.gitconnected.com/build-a-personal-website-with-github-pages-and-hugo-6c68592204c7) by Yuanyuan Ge, for which I kept a step-by-step journal [[Web Publishing With Github Pages and Hugo\|here]]
  #project/aborted ==I decided to abandon this project after trying for hours to deal with all the Github push/commit/password/publish problems.==
    1.  [Configuring a Custom Domain for your Github Pages Site](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)
3.  Make the public folder of your Quartz repo a submodule of that repo
    1.  `git submodule add <your_github_project_url> ./public`
4.  Install Hugo for minifying and running a local server
    1.  `brew install hugo`
5.  Clone obsidian-export wherever you keep libraries
    1.  Obsidian Export runs in _Rust_, so make sure you have Rust enabled on your machine
    2.  If I remember correctly, I ran `cargo build` from the obsidian-export directory to build a local binary that can be called in the compile script
6.  Clone obsidian-hugo wherever you keep libraries
    1.  Obsidian-hugo runs in _Go_, so make sure you have Go enabled on your machine and in your PATH;
    2.  The watch/compile script will run `go run ~/Sites/hugo-obsidian -input=/Users/brandonkboswell/Sites/quartz/content -output=/Users/brandonkboswell/Sites/quartz/assets/indices -index -root=/Users/brandonkboswell/Sites/quartz;` when it compiles.
7.  Update the compile and watch scripts for the paths of your folders
    1.  My quartz directory is at: ~/Sites/quartz
    2.  My Obsidian Vault is at (My _iCloud_ Folder): ~/Library/Mobile\ Documents/iCloud~md~obsidian/Documents/bkb
    3.  My hugo-obsidian directory is at: ~/Sites/hugo-obsidian
8.  Configure your configuration files
    1.  **Hugo Config** — quartz/config.toml file
    2.  **Quartz Config** — data/config.yaml
    3.  **Quartz Graph Config** — data/graphConfig.yaml
9.  Add a file name **.export-ignore** to your Obsidian Vault
    1.  Obsidian Export will skip any files / folders you mention here and make sure they don’t get handed to Quartz
    2.  You can’t create this file in Obsidian (you likely want to use the finder or a Code Editor).
    3.  A sample of my .export-ignore file is further down in this article
10.  Run the watch script (which will do an initial compile and then watch for changes to your Obsidian Vault)
    1.  Note that the compile script empties out your quartz/content directory so that files that may have been moved or deleted from your Obsidian Vault do not end up being pushed to the public internet. **Make sure that this path is set correctly before running the watch or compile script.**
11.  Start a hugo server from your quartz directory
    1.  `./serve.sh`
12.  Assuming everything worked, you should be able to preview your vault at: localhost:1313
13.  Tinker / tweak for way too long
14.  When you’re ready you can commit your quartz/public directory to Github pages
    1.  **Verify _(especially for the first commit)_ that there is nothing private that you don’t want uploaded to the internet.**
    2.  `cd ~/Sites/quartz/public; git add .; git commit -m "Update"; git push origin`

---

## Configure your .export-ignore file at the root of your Obsidian Vault. Here’s mine:

```
 1
 2
 3
 4
 5
 6
 7
 8
 9
10
11
12
13
14
15
```

```fallback
templates/*
private/*
1-1/*
business/*
collections/*
people/*
to_publish/*
files/*
temporal/*
personal/*
screenshots/*
ideas/*
.trash/*
.obsidian/*
_content_calendar.md
```


## To compile your notes once

```
1
2
3
4
5
6
7
8
9
```

```
#!/bin/bash

cd ~/Sites/quartz; ./compile.sh

--- compile.sh ---

#!/bin/bash

cd ~/Sites/hugo-obsidian; rm -fr ~/Sites/quartz/content/*; rm -rf ~/Sites/quartz/public/*; ~/Sites/obsidian-export/target/debug/obsidian-export --add-titles --frontmatter=always ~/Library/Mobile\ Documents/iCloud~md~obsidian/Documents/bkb ~/Sites/quartz/content; go run ~/Sites/hugo-obsidian -input=/Users/brandonkboswell/Sites/quartz/content -output=/Users/brandonkboswell/Sites/quartz/assets/indices -index -root=/Users/brandonkboswell/Sites/quartz; (cd ~/Sites/quartz && hugo --minify)
```


## To recompile your notes on change

```
1
2
3
4
5
6
7
```

```
cd ~/Sites/quartz; ./watch.sh

--- watch.sh ---

#!/bin/bash

export GOPATH=/Users/$USER/go; export GOROOT="$(/usr/local/bin/brew --prefix golang)/libexec"; export PATH="$PATH:${GOPATH}/bin:${GOROOT}/bin"; cd ~/Sites/quartz; nodemon -w ~/Library/Mobile\ Documents/iCloud~md~obsidian/Documents/bkb -w ~/Sites/quartz/assets/js -w ~/Sites/quartz/assets/styles -w ~/Sites/quartz/layouts -w ~/Sites/quartz/config.toml -w ~/Sites/quartz/data/config.yaml -x "~/Sites/quartz/compile.sh" -e md,html,js,scss,xml
```


## To preview your changes before pushing to Github, you can run a local hugo server:

Sometimes the server will crash while the compile script is rebuilding everything. If you wrap the hugo server code in a while loop then it will restart itself if this happens. For this I will have two terminal panes open on for the watch script and one for the hugo server. As I make changes to my Obsidian Vault or the Quartz files it will recompile the content and then hugo will recompile, at which point you can refresh your browser to see the change. Usually that will be at localhost:1313.

```
1
2
3
```

```
(while true; do 
	hugo server --disableFastRender
done) &
```

## When I’m ready to publish an update to [[GitHub\|Github]]:

Go to the garden folder and commit those changes:

```
1
```

```
cd ~/sites/quartz/public; git add .; git commit -m "Update"; git push origin
```

## Additional Notes

-   You probably want to do your ignoring of personal files at the obsidian-export level because if a file is referenced in another file, but that file is flagged as a draft in the frontmatter then hugo-obsidian will have trouble with that and make hugo error on compile with the backlinks. Doing your ignoring of specific files in obsidian-export takes care of this.
-   If you’ve never used _Hugo_ before (like I hadn’t prior to this project), you may not know that Hugo has a static folder that generates assets you want to be in any subsequent rebuilds. When I first started this project I added a bunch of lines to the compile script to create files and moving files around when all I really needed to do was add those files to my static folder.
-   You are going to want to update your Hugo layout files to take advantage of the backlink rendering provided by Obsidian Export. The changes you’ll want to make, plus an explanation are available here: [https://github.com/zoni/obsidian-export/issues/8#issuecomment-774521792](https://github.com/zoni/obsidian-export/issues/8#issuecomment-774521792)

## Previous Attempts

-   Originally I modified hugo-obsidian to get around the no titles issue, since I now do this in obsidian-export I no longer need to maintain a fork of that code. If it’s useful to you, here is the change I made:
    -   I had to make a minor modification to obsidian-hugo because it assumes that all of your files have a title attribute in their frontmatter. Unfortunately, most of my files do not have this title front matter. I have a branch of obsidian-hugo that uses the file’s name to generate titles if that frontmatter is not present. [https://github.com/brandonkboswell/hugo-obsidian/tree/without_titles](https://github.com/brandonkboswell/hugo-obsidian/tree/without_titles). _As the time of this writing, that branch has not been merged into the main repo, but it may have by the time you’re reading this._)

#source/dupe/end 