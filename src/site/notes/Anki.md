---
{"dg-publish":true,"permalink":"/anki/","created":"","updated":""}
---


[[Anki\|Anki]] is the third [[PKM\|PKM]] that I built, after [[DTSearch\|DTSearch]] and [[Evernote\|Evernote]]. Today, it is my most frequently used and updated system. I almost stopped using [[DTSearch\|DTSearch]] altogether for its being on the old [[Windows 10 VM\|Windows 10 VM]], a resource hog on my [[Mid-2014 MacBook Pro\|Mid-2014 MacBook Pro]]. As for [[Evernote\|Evernote]], it is where garbage data goes to die. I still use it today, making most of the free 60MB storage per month to store random web content and short memos.

I started putting all my effort into [[Anki\|Anki]] in ... 2019, when I successfully imported 200,000 English-Chinese dictionary entries into it and started liking its versatility. The rest is history. 

Now I have this as my second weapon: [[EKLIAO\|My first Obsidian vault: EKLIAO]].

---
## Anki hacks I've learned
*(New to old)*

- image occlusion ([[Cloze\|Cloze]])
	- add-on: image occlusion advanced
- hierarchical tags: simply rename a tag with two colons in the middle. Can be multiple levels, e.g.:

	![anki hierarchical tags vs flat tags w arbitrary delimiters.png](/img/user/_attachments/anki%20hierarchical%20tags%20vs%20flat%20tags%20w%20arbitrary%20delimiters.png)

- rename or delete a tag in browser left-nav tag list (without bulk adding a new tag then bulk deleting the old tag)
- use [[Anki add-on - Customize keyboard shortcuts\|Anki add-on - Customize keyboard shortcuts]]
	- to change default [[keyboard shortcut\|keyboard shortcut]] for [[Cloze deletion - different card\|Cloze deletion - different card]] for "adding [[Cloze deletion - different card\|Cloze deletion - different card]]" to `Cmd+Shift+Z`
- change font color in the styling section of a [[note type\|note type]]
- add [[Cloze deletion - different card\|Cloze deletion - different card]]
- add [[Cloze deletion - same card\|Cloze deletion - same card]]

## Hierarchical tags and search

- Truly hierarchical: searching for `tag:A` alone without saying `tag:A::` or `tag:A*` will still get `A::B` and `A::B::C`, etc. Great!
 ![hierarchical tag search in anki.png](/img/user/_attachments/hierarchical%20tag%20search%20in%20anki.png)
