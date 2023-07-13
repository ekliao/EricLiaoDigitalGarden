---
{"dg-publish":true,"permalink":"/limit-to-the-total-number-of-obsidian-files/","noteIcon":"2","created":"","updated":""}
---

# Have I hit Obsidian file limit?

As I experiment with a vault dedicated to dictionaries and reference materials, I seem to have hit a wall. My desktop Obsidian hangs and wouldn't get past loading, when total number of notes is...

- 384K (after two days of iCloud syncing) - not responsive
- 378K - same as above; saa
- 346K - (slowly) loading cache... eventually still stuck

Meanwhile, the iPhone/iPad app loaded but hanged frequently at the 346k level. iOS performance doesn't matter that much. It's the desktop that must have decent performance.

- 315K - saa
- 228K - saa
- 86K - saa

At this point, I am declaring that this vault is damaged beyond repair, because previously I had a vault with 150K that eventually loaded and worked fine. 86K can't be the limit! My initial dump of 384K must have ruined it. Luckily, Obsidian vault management, being local file based, is a piece of cake. It's iCloud that's always the pain.

# Alternative: the gradual approach

I created a new vault, and started adding folders/files gradually...

- 25K - OK after showing indexing
(Next, a big jump in files because of bigram Chinese entries of almost 90K)
- 115K - OK. As shown. It worked after it completed indexing, which is always slow and sporadic, but at least an indication of action.

![../_attachments/Screen Shot 2023-07-11 at 05.11.07.png|250](/img/user/_attachments/Screen%20Shot%202023-07-11%20at%2005.11.07.png)

- 180K - OK
- 228K - OK
- 267K - OK

Almost 300K. A new milestone!

- 469K - In progress...until it hanged eventually with the screen turning blank

Paring down...

- 442K - In progress...seems to be heading toward hanging

Paring down...

- 419K - A welcome sign of life:

![_attachments/Screen Shot 2023-07-12 at 15.57.20.png](/img/user/_attachments/Screen%20Shot%202023-07-12%20at%2015.57.20.png)

But alas it blanked out in the end. 

- 388K - Watched it successfully load and index. Then, the search experience (CMD-o) was horrible, with a lag of 10-60 seconds just to find a note and open it. There is no way I can use it. This is the end of the iCloud experiment for ~400K files.

### Don't disturb the indexing

Here's a tip: If a file is found, appears to be opened, but content isn't showing, consider waiting until the indexing is done. Don't wreck it.

![[../_attachments/obsidian not showing file content - indexing in progress.mp4]]

While this problem occurred, iCloud is busy too.

![../_attachments/Screen Shot 2023-07-11 at 06.50.48.png|600](/img/user/_attachments/Screen%20Shot%202023-07-11%20at%2006.50.48.png)


### iCloud-caused reindexing observed

Closing the app and restart: the famed reindexing happened, as predicted by dev:

![_attachments/Screen Shot 2023-07-12 at 18.01.40.png](/img/user/_attachments/Screen%20Shot%202023-07-12%20at%2018.01.40.png)


## Conclusion: Obsidian on iCloud for 300~400K files = dead end

It's enough pain so far to decide to go against an Obsidian vault with at least 400K files on iCloud. To have a dictionary database with English words and phrases, and Chinese terms, the total number of entries naturally goes toward one million. If I include professional terminology from various fields, the number blows up to over two millions (think 金山詞霸). A 400K limit isn't going to cut it. I am hinging all my hope on the off-iCloud local vault.

# Alt-alternative approach

I had an idea. If, as I learned, iCloud is the culprit in slow initializing and indexing, how about a pure local vault that does not require syncing? I set out to test it, dumping a huge load in one fell swoop:

- 387K - Progress bar hanged. Not a good sign. Reducing files.
- 289K - OK

By the way, this number happens to be a tad more than the limit reported by someone who actually tried it and experienced extremely slowness, at [280,986](https://forum.obsidian.md/t/maximum-number-of-notes-in-vault/1509) files.

Yay! I know it's going to be okay, because the indexing (onetime) progress finally presented itself after some wait for the initial progress bar (loading vault, workspace, cache, etc.).

![../_attachments/Screen Shot 2023-07-11 at 14.01.36.png|500](/img/user/_attachments/Screen%20Shot%202023-07-11%20at%2014.01.36.png)

And, I observed a much appreciated new behavior: while indexing, the `CMD-O` search and open found this entry and opened it right away:

![../_attachments/Screen Shot 2023-07-11 at 14.05.29.png|600](/img/user/_attachments/Screen%20Shot%202023-07-11%20at%2014.05.29.png)

This is so uplifting! Next, attempting the one-third million milestone:

- 355K - OK - very slooooww, and file content doesn't show any more.

While I wait for good news, I found someone demanding 500K:

#Glasp 
### Indexing Large Number of Files - Still Not Working

#### Metadata
- Title: Indexing Large Number of Files - Still Not Working
- Tags: #Obsidian, #limit
- URL: https://forum.obsidian.md/t/indexing-large-number-of-files/47397

#### Page Comment
- I feel his pain. 500K files. My dream is 800K for my current plan of combined dictionaries.

#### Highlights & Notes
- Expected result: I need the obsidian app to handle >500K files

---

The OP's use case is also linguistic. Great minds think alike? 😆 But can I up the ante? As my Glasp page comment says, my goal is at least 800K. 

- 535K - New limit - In progress... hanged (without the indexing progress)

Paring down...

- 442K - In progress... until 10 hours later when the progress died with screen turning blank. The hang was caught with this screen recording:

![[../_attachments/ob-local-index-turns-blank-after-10hrs 2.mp4]]

Shut the app window. Restarted it. This time, I learned for the first time that it did make progress indexing despite the "hang." It now starts with 171K files remaining to index instead of 442K, meaning the previous attempt was at least 60% complete.


