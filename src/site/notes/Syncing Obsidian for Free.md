---
{"dg-publish":true,"permalink":"/syncing-obsidian-for-free/","noteIcon":"2"}
---

Syncing Obsidian vaults between devices, especially desktop and mobile.

## iCloud


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/10-dailynotes/2023-04-20/#b836ee" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



### How to sync an Obsidian vault between MacOS desktop and iOS for free

</div></div>
 

### Error: "iCloud disabled for Obsidian" on iOS/iPadOS?
#paste/glasp 
![75](https://forum.obsidian.md/uploads/default/original/1X/bf119bd48f748f4fd2d65f2d1bb05d3c806883b5.png)

### Metadata
- Title: iCloud disabled for Obsidian?
- Tags: #iCloud, #ob, #iOS, #iPadOS
- URL: https://forum.obsidian.md/t/icloud-disabled-for-obsidian/17395

### Highlights & Notes
- That error message only shows up when your iOS device has blocked Obsidian from using iCloud. You can change the setting from iOS’s system settings app > Your Apple ID > iCloud > Make sure that “iCloud Drive” and “Obsidian” are both turned on.

---
### iCloud path

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

---
## ~~Dropbox~~

I initially set up my desktop Obsidian vaults on [[Dropbox\|Dropbox]], but haven't found any workable solution for syncing it to mobile devices, so I moved Obsidian to [[iCloud (Drive)\|iCloud (Drive)]]. It's been almost smooth sailing since, with the exception of sluggishness and constant indexing.

Update: Dropbox Obsidian vault on iOS: [can't be done](https://forum.obsidian.md/t/mobile-app-for-iphone-sync-with-dropbox/18676/3)