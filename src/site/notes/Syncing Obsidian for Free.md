---
{"dg-publish":true,"permalink":"/syncing-obsidian-for-free/","created":"","updated":""}
---

## iCloud


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/10-dailynotes/2023-04-20/#b836ee" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



### How to sync an Obsidian vault between MacOS desktop and iOS for free

</div></div>
 

## iCloud directory

Though the Obsidian vault on iCloud on the Mac appears to be under
```
iCloud Drive/Obsidian/<vault>
```
as shown in `Finder`:

![Screen Shot 2023-04-22 at 17.53.18.png|400](/img/user/_attachments/Screen%20Shot%202023-04-22%20at%2017.53.18.png)

The actual folder is actually here:
```
/Users/<username>/Library/Mobile Documents/iCloud~md~obsidian/Documents/<vault>
```

This is the path that a diff tool such as [[Beyond Compare\|Beyond Compare]] needs to point to in order to find files.