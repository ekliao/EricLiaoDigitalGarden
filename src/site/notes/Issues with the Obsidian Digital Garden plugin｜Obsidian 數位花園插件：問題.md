---
{"dg-publish":true,"permalink":"/issues-with-the-obsidian-digital-garden-plugin-obsidian/","noteIcon":"2"}
---

*(New to old)*

- 🔥 *2024-01-17* [[Obsidian Digital Garden plugin - Certain characters in note name won't work (empty page) but will build successfully on Netlify｜數位花園頁名不允許某些合法字元\|Obsidian Digital Garden plugin - Certain characters in note name won't work (empty page) but will build successfully on Netlify｜數位花園頁名不允許某些合法字元]]

- Buggy implementation in the Publication Status on both the desktop and iOS. Problem: the same entry should not appear twice, e.g.

### Desktop

![[_attachments/Screen Shot 2023-06-21 at 00.05.47.png\|400]]
### iOS

![[_attachments/ios digital garden publication status - bogus and dupes.jpeg\|300]]

- Persistent discrepancy between Publication Status of in the desktop and iOS, even after iCloud has synced everything, e.g.

### Desktop
![[_attachments/Screen Shot 2023-06-20 at 13.53.16.png\|300]]

### iOS
![[_attachments/IMG_292E3811A99C-1.jpeg\|250]]

Here, the iOS status is wrong, because the 2023-05-22.md page is live and well on the published site.

- _2023-06-17_ I experienced for the first time trouble publishing an image saved in .PNG. Had to resave it as .JPG and resize it (into 600) before it finally showed up on the website. I don't really know what the issue is. Will watch this closely.

- Occasionally due to browser caching, what's actually published isn't what the desktop browser (Chrome) shows, involving wrong links. If this happens, simply clearing browser's "cached images/files" will clear the issue.

- The Publication Status popup becomes sluggish after 100+ notes in the published garden, taking some 15-20 seconds to show updated counts. But, clicking ahead on the buttons to publish new and changed notes before seeing the final count *does* seem to have an effect. Keep doing this but keep watch.
	- 2023-06-01: Strangely, despite being much more sluggish on the iOS, the popup is actually more responsive there. If the desktop seems stuck, try the iOS to get published sooner.

- 🤷 Any Glasp URL don't work as links. The html URL is exposed raw. Not a disaster, just ungainly and inconvenient.

- ☠️ The Search bar at the top of the left-nav-pane does not work for all non-CJK words, even simple single-word queries. Some works, others don't. It's hit-and-miss. And, mostly annoyingly, it does not work at all for Chinese. 


<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">




*(begin rants)*
Hello? It's 2023, not 1990s any more! It's no longer a time when Unicode just emerged and gradually heading towards its eventual domination over entire world of web, driving out legacy encodings like Big5. Non-Unicode-aware websites and search functionality have NO PLACE in this world! 
*(end rants)*

</div></div>
