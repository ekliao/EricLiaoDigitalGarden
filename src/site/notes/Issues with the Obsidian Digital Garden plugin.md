---
{"dg-publish":true,"permalink":"/issues-with-the-obsidian-digital-garden-plugin/","noteIcon":"2","created":"","updated":""}
---

*(New to old)*

- Buggy implementation in the Publication Status on both the desktop and iOS. Problem: the same entry should not appear twice, e.g.

### Desktop

![_attachments/Screen Shot 2023-06-21 at 00.05.47.png|400](/img/user/_attachments/Screen%20Shot%202023-06-21%20at%2000.05.47.png)
### iOS

![_attachments/ios digital garden publication status - bogus and dupes.jpeg|300](/img/user/_attachments/ios%20digital%20garden%20publication%20status%20-%20bogus%20and%20dupes.jpeg)

- Persistent discrepancy between Publication Status of in the desktop and iOS, even after iCloud has synced everything, e.g.

### Desktop
![_attachments/Screen Shot 2023-06-20 at 13.53.16.png|300](/img/user/_attachments/Screen%20Shot%202023-06-20%20at%2013.53.16.png)

### iOS
![_attachments/IMG_292E3811A99C-1.jpeg|250](/img/user/_attachments/IMG_292E3811A99C-1.jpeg)

Here, the iOS status is wrong, because the 2023-05-22.md page is live and well on the published site.

- _2023-06-17_ I experienced for the first time trouble publishing an image saved in .PNG. Had to resave it as .JPG and resize it (into 600) before it finally showed up on the website. I don't really know what the issue is. Will watch this closely.

- Occasionally due to browser caching, what's actually published isn't what the desktop browser (Chrome) shows, involving wrong links. If this happens, simply clearing browser's "cached images/files" will clear the issue.

- The Publication Status popup becomes sluggish after 100+ notes in the published garden, taking some 15-20 seconds to show updated counts. But, clicking ahead on the buttons to publish new and changed notes before seeing the final count *does* seem to have an effect. Keep doing this but keep watch.
	- 2023-06-01: Strangely, despite being much more sluggish on the iOS, the popup is actually more responsive there. If the desktop seems stuck, try the iOS to get published sooner.

- 🤷 Any Glasp URL don't work as links. The html URL is exposed raw. Not a disaster, just ungainly and inconvenient.

- ☠️ The Search bar at the top of the left-nav-pane does not work for all non-CJK words, even simple single-word queries. Some works, others don't. It's hit-and-miss. And, mostly annoyingly, it does not work at all for Chinese. 


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/hello-it-s-not-1990s-any-more/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




*(begin rants)*
Hello? It's 2023, not 1990s any more! It's no longer a time when Unicode just emerged and gradually heading towards its eventual domination over entire world of web, driving out legacy encodings like Big5. Non-Unicode-aware websites and search functionality have NO PLACE in this world! 
*(end rants)*

</div></div>
