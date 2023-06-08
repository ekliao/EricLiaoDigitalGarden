---
{"dg-publish":true,"permalink":"/obsidian-issues/","noteIcon":"2","created":"","updated":""}
---

*(new to old)*

## Tags in file name and in metadata don't work as tags

The pound sign (\#) for tags in file name is allowed if the file is directly copied under vault externally. Despite this, it does not work as tags in OB, e.g.:

![../../../_attachments/Screen Shot 2023-06-08 at 15.59.07.png|500](/img/user/_attachments/Screen%20Shot%202023-06-08%20at%2015.59.07.png)

---
## iCloud free sync is often stuck in synchronizing the Obsidian configuration files

This view on my iPhone has become a daily eyesore:

![_attachments/IMG_EAE1F33EA278-1.jpeg|250](/img/user/_attachments/IMG_EAE1F33EA278-1.jpeg)
- [The problem, and two potential solutions using Github (manual sync) and Apple Scriptable](https://www.reddit.com/r/ObsidianMD/comments/vdal97/is_there_a_way_to_shorten_this_waiting_time_or/)

## Hierarchical tags

Metadata hierarchical tags can't be searched through the hashtag syntax

#paste/glasp 
#### Tags - Obsidian Help
##### Metadata
- Title: Tags - Obsidian Help
- Tags: #Obsidian, #issue
- URL: https://help.obsidian.md/Editing+and+formatting/Tags

##### Highlights & Notes
- Nested tags Nested tags define tag hierarchies that make it easier to find and filter related tags.  Create nested tags by using forward slashes (/) in the tag name, for example #inbox/to-read and #inbox/processing.  Both the Search and Tags plugins support nested tags.
#paste/e 
---
That's the official documentation, but this is what I saw:
e.g. although the following hierarchical tag `d/x` in the metadata section of a note

`tag: d/x, vocab1, vocab2`

is findable by

`tag:d/x`

search syntax, it is ==not found== by the

`#d/x` 

syntax. But the same hierarchical tag outside the metadata section, expressed as hashtag:

#d/x 

can be found by both

`tag:d/x` and `#d/x` syntax. See how the result contradicts the official doc?

Conclusion: ==Avoid using hierarchical tags inside metadata== for maximum tag findability.

---
## Live preview fails

- *(05-21, 2023-04-27)* [live preview not working](https://forum.obsidian.md/t/live-preview-not-working-despite-resetting-editor-mode-disabling-plugins-etc/32922)

When "live preview" fails, it means what's depicted in this screenshot is not true:
- Can edit
- Showing nice formatting
- Page settings (three-dots menu): Both Reading view and Source mode are OFF

![_attachments/Screen Shot 2023-05-21 at 11.30.38.png](/img/user/_attachments/Screen%20Shot%202023-05-21%20at%2011.30.38.png)

#solution/worked
	 - [one solution: toggle legacy editor, relaunch, and toggle back](https://forum.obsidian.md/t/live-preview-stopped-working-toggling-legacy-editor-fixed-it/30377)
	
## Dictionary lookup

- See how the word 'well' is not in the dictionary
#issue/gone (2023-04-16)
> ![Screen Shot 2023-02-28 at 11.47.17 PM.png](/img/user/_attachments/Screen%20Shot%202023-02-28%20at%2011.47.17%20PM.png)

---

# More...
### Issues Others Reported
- [multilingual notes or content](https://www.reddit.com/r/ObsidianMD/comments/wlm56w/bilingual_or_multilingual_people_how_do_you_deal/)