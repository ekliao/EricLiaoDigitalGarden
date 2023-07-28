---
{"dg-publish":true,"permalink":"/anki-anki-web-cloud-storage-file-size-limit-official-and-actual/","noteIcon":"2","created":"","updated":""}
---

creation-date:: 2023-07-28

Over the years I have enjoyed a larger limit than officially advertised. So, I have no complaint. I just need to avoid the trigger of whole-collection upload as much as possible, because it really is a pain in the neck.

# Official limit is 250MB

#paste/b 
#### [Are there limits on file sizes on AnkiWeb?](https://faqs.ankiweb.net/are-there-limits-on-file-sizes-on-ankiweb.html#are-there-limits-on-file-sizes-on-ankiweb)

Collections on AnkiWeb are limited to a compressed size of 100MB, and an uncompressed size of 250MB. This includes the text on your cards and the scheduling information, but does not include sounds/images, as they are stored separately.

Most users will never reach the limit. 25,000 average-sized cards and several years of review history will take up about 25MB, so to hit the limit you usually need to either be copying large amounts of text into each card, or filling your collection with hundreds of thousands of new cards that you aren't actually studying.

At the moment there are no limits on the size of your media, although the size of individual media files is limited to 100MB.

As the usage of Anki and AnkiWeb increases, at some point a pricing system may be introduced where basic, low-capacity accounts are free and heavier users can pay more for more space.

If you have hit the collection size limit, you will see messages about the collection being in an inconsistent state when you do a one way upload to AnkiWeb. It is not possible to increase the limit, because such large collections slow down AnkiWeb for other users. If you have imported a dictionary's worth of content, you will need to move some unused cards to a separate deck, export the deck, and then delete the deck from your collection. After doing so, Tools>Check Database can be used to free up space that was taken by the deleted cards.
#paste/e 

# Actual limits from my experience

## Forced whole-collection upload

About 315MB, higher than 250MB.

## Normal sync

The limit is even greater. I've had Ankiweb accept my collection size up to 480MB. It kept growing larger and larger over time. Caveat: if somehow whole-collection upload is triggered, it'll enforce the 315MB limit again. I would have to jump through some hoofs to slim down then add incrementally.

### What forces whole-collection upload?

Any change of note type locally, even for just one card, will force such an upload.

#### Hack: How to avoid a whole-collection upload

Export the deck to a new profile, change the note type there, and import back to main profile. As long as there is no "note type change" in the main profile, there no trigger.
