---
{"dg-publish":true,"permalink":"/anki/","noteIcon":"2","created":"","updated":""}
---

[[Anki\|Anki]] is the third [[PKM\|PKM]] that I built, after [[DTSearch\|DTSearch]] and [[Evernote\|Evernote]]. Today, it is my most frequently used and updated system. I almost stopped using [[DTSearch\|DTSearch]] altogether for its being on the old [[Windows 10 VM\|Windows 10 VM]], a resource hog on my [[Mid-2014 MacBook Pro\|Mid-2014 MacBook Pro]]. As for [[Evernote\|Evernote]], it is where garbage data goes to die. I still use it today, making most of the free 60MB storage per month to store random web content and short memos.
{ #2bb266}


I started putting all my effort into [[Anki\|Anki]] in ... 2019, when I successfully imported 200,000 English-Chinese dictionary entries into it and started liking its versatility. The rest is history. 

Now I have this as my second weapon: [[Vault home - Ekliao\|My first Obsidian vault: EKLIAO]].

# Verdict: 4 stars

# Pro

## AnkiWeb surprisingly fast

- Having experienced the awful slowness of Obsidian (iCloud and local) in handling 400K data, I gave AnkiWeb a try. It's already there, but I actually never used it, assuming it wasn't going to be fast compared to the desktop app. Gosh, I was so wrong. On 1.2 million entries, the search for a headword takes less than 5 seconds, sometimes only 1-2 seconds. What a surprise!
- More about [[AnkiWeb\|AnkiWeb]] (its pros and cons).

## Hierarchical tags and search

- Truly hierarchical: searching for `tag:A` alone without saying `tag:A::` or `tag:A*` will still get `A::B` and `A::B::C`, etc. Great!
 ![hierarchical tag search in anki.png](/img/user/_attachments/hierarchical%20tag%20search%20in%20anki.png)
# Cons
## Very limited regex search

#Glasp 
### Searching - Anki Manual

#### Metadata
- Title: Searching - Anki Manual
- Tags: #Anki, #regex, #regular-expressions
- URL: https://docs.ankiweb.net/searching.html
#### Highlights & Notes
- "re:(some|another).*thing"

#### Page Comment
Despite Anki's official documentation, Anki does not support parentheses at all. I have tried many times and have given up. Parentheses for grouping (either capturing or non-capturing kind) is crucial in regex searching.

## Random ideas of metacharacters in regex search
- Simply put, Anki's search has the weirdest idea of what works and what doesn't. For example, a literal space won't work in a regex search. Don't get me started.

## No "search as you type" functionality

---
# Migrating to Obsidian
- [[Anki to Mochi to Obsidian\|Anki to Mochi to Obsidian]]

# Anki hacks I've learned
*(New to old)*

- [[Anki - AnkiWeb (cloud storage) file size limit - official and actual\|Anki - AnkiWeb (cloud storage) file size limit - official and actual]]

- [[Anki - (Basic) note type naming mess (variants without a difference)\|Anki - (Basic) note type naming mess (variants without a difference)]]

- User interface size
	- Though obvious, I didn't discover this adjustable parameter earlier. Once I changed it to 150%, Anki immediately felt a lot more accessible.

![_attachments/Screen Shot 2023-06-16 at 12.43.32.png|350](/img/user/_attachments/Screen%20Shot%202023-06-16%20at%2012.43.32.png)

- "Set font size" add-on (enlarges everything except browser grid font/back fields)

- Image occlusion ([[Cloze\|Cloze]])
	- add-on: image occlusion advanced

- Hierarchical tags: simply rename a tag with two colons in the middle. Can be multiple levels, e.g.:

	![anki hierarchical tags vs flat tags w arbitrary delimiters.png|250](/img/user/_attachments/anki%20hierarchical%20tags%20vs%20flat%20tags%20w%20arbitrary%20delimiters.png)

- Rename or delete a tag in browser left-nav tag list (without bulk adding a new tag then bulk deleting the old tag)

- Use [[Anki add-on - Customize keyboard shortcuts\|Anki add-on - Customize keyboard shortcuts]]
	- to change default [[Keyboard shortcuts\|Keyboard shortcuts]] for [[Cloze deletion - different card\|Cloze deletion - different card]] for "adding [[Cloze deletion - different card\|Cloze deletion - different card]]" to `Cmd+Shift+Z`

- Change font color in the styling section of a [[note type\|note type]]

- Add [[Cloze deletion - different card\|Cloze deletion - different card]]

- Add [[Cloze deletion - same card\|Cloze deletion - same card]]

# Add-ons

- [[Merging Notes： Anki Add-ons of Interest\|Merging Notes： Anki Add-ons of Interest]]
---

# More ...

[[Ankification\|Ankification]]

[[Anki Export Considerations： text vs apkg\|Anki Export Considerations： text vs apkg]]

[[Anki data merging project (WIP w ongoing change log)\|Anki data merging project (WIP w ongoing change log)]]



