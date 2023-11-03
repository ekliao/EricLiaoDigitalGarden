---
{"dg-publish":true,"permalink":"/anki-issues-of-slow-desktop-app/","noteIcon":"2"}
---

date-created:: 2023-08-10

Aiyaa! A dark day for Anki. Just when I expressed my renewed interest and appreciation of [[Anki\|Anki]], it pulled this stunt on me! :-(

## *(2023-08-10)* Sudden slowdown of desktop on browser and search

This inexplicable degradation happened suddenly today, after I had added TwMoeD (Mandarin) for weeks. I also haven't installed any new add-ons lately.

Incredible... Now it's a long wait to even open the browser. What's more appalling: More than 1 minute for any search! (Used to be 6-7 seconds).

I tried restoring from backup. No joy.
### Emergency remedy

Keep slimming down until the collection isn't oversized:
- The limit seems to be 314.5MB (consistent behavior)

![_attachments/Screen Shot 2023-08-10 at 12.36.16.png|200](/img/user/_attachments/Screen%20Shot%202023-08-10%20at%2012.36.16.png)

Slim down main profile by moving these decks to ekliao+2:

- Taigi
- MoeD（Mandarin）
- JMYH
- Note-taking
- XSHJHY

After unloading these, the main profile was able to do a full sync (required, after restoring from backup) to AnkiWeb.

Stats:
- Backup size: 124.4MB
- Database (Collection.anki2): 293.5MB < 314.5MB.
#### Beyond repair

After slimming, at least 30 seconds for "front:" search. Too slow still!

At this point, I realized there's no going back to the 6-7 second search. I don't know what happened, but it is what it is.

Luckily, [[AnkiWeb\|AnkiWeb]] search interface is usable, and is blazing fast.

## New drastic remedy

I decided to pull a Hail Mary fix just out of curiosity to see if it works:

- Make sure the cloud has the latest main profile.
- Rename the old Anki2 folder (in application support) as Anki2old.
- Delete the Anki app.
- Install it.
- Start it.
- Press Sync. Prompted to log in.
- Select "download from web."
### Result

Like magic, this time a typical full text (not "front:") search took 1-2 seconds, even much better than the 6-7 seconds I had been "used to."

### Follow-up action

- Use [[Beyond Compare\|Beyond Compare]] on Anki2old and the new Anki2 folders.
- Move all data under root folders of profile names to the new folder.
- Don't move add-ons.
- There are strange .m3u files that seem to be playlists for audio. Don't know what they are. But it's harmless to move.

![_attachments/Screen Shot 2023-08-10 at 20.28.23.png|400](/img/user/_attachments/Screen%20Shot%202023-08-10%20at%2020.28.23.png)
# Moral of the story

Software performs in mysterious ways. Try reinstalling before giving up.

I think the accumulation and combination of certain add-ons dragged down the database performance, the cause of which was unknowable to me.

This degradation has happened to me only once in the 3+ years of active use. I guess that is acceptable, especially now that I've identified the proper remedy.

For the record, these are the Anki add-ons I'm walking away from:

![_attachments/anki addons i discarded on 20230810 when reinstalling to restore fast speed of desktop.png|400](/img/user/_attachments/anki%20addons%20i%20discarded%20on%2020230810%20when%20reinstalling%20to%20restore%20fast%20speed%20of%20desktop.png)

And finally for sanity check, the cloud storage version does preserve each and every media file, as proved from the "no diff" status of the "collection.media" folder:

![_attachments/Screen Shot 2023-08-10 at 20.40.48.png|400](/img/user/_attachments/Screen%20Shot%202023-08-10%20at%2020.40.48.png)

---

[[Anki add-on performance tracking\|Anki add-on performance tracking]]