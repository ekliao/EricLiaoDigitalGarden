---
{"dg-publish":true,"permalink":"/ob-tips-and-hacks-i-ve-got/","noteIcon":"2","created":"","updated":""}
---

*(New to Old)*

- Pasting tables


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/10-dailynotes/2023-06-14/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">

$<div class="markdown-embed-title">

# 2023-06-14

</div>



#meta/ob 
# Copying and pasting tabular data into Obsidian

What a delight! In researching a term ("oxycodone"), I selected partial tabular data from a web page and copy-and-pasted into Obsidian, expecting to do some manual tweaking, but look at this table:

![../_attachments/Screen Shot 2023-06-15 at 12.26.20.png](/img/user/_attachments/Screen%20Shot%202023-06-15%20at%2012.26.20.png)
## Post-editing
What's left for me to do is edit and add one vertical bar to fix the alignment problem, and voilà! It's as good as it gets. The visual elements (pictures) are nicely dealt with as linked images.

![../_attachments/Screen Shot 2023-06-15 at 12.30.10.png](/img/user/_attachments/Screen%20Shot%202023-06-15%20at%2012.30.10.png)

</div></div>


- In the file pane, drag a file/note into the editor pane to get a link to its name (`![[file-name]]` and then remove the link
	  e.g. for copying the PDF file name into the required `annotation-target:` frontmatter field in order to use the `Annotator` plugin to annotate the PDF in OB.
	  
- Creating real links to a potentially unconnected note from unlinked mentions in the right-nav-pane
#project/learn-by-doing 
#project/completed 
#created/video
![[obsidian - creating real links to a potentially unconnected note from unlinked mentions.mp4]]

- Using right-nav-pane Tag Wrangler plugin (#) to rename a tag globally including making it nested! Powerful
![Screen Shot 2023-04-16 at 11.29.31 AM.png](/img/user/_attachments/Screen%20Shot%202023-04-16%20at%2011.29.31%20AM.png)

- [nested tags](https://help.obsidian.md/Editing+and+formatting/Tags#Nested+tags) (/)
- [embedding a note](https://help.obsidian.md/Linking+notes+and+files/Embedding+files), or a [heading](https://help.obsidian.md/Linking+notes+and+files/Internal+links#Link+to+a+heading+in+a+note) or a [block](https://help.obsidian.md/Linking+notes+and+files/Internal+links#Link+to+a+block+in+a+note) of a note (! followed by usual double square-brackets), or embedding internal files (different formats) in general
	- Advantage: avoiding content duplication. *Write once, reference anywhere.*
		- Application: write something in a daily note and refer to it through embedding, because daily notes have the feel of chronologically documenting living, discovery, learning, and progress.
- [alias](https://help.obsidian.md/Linking+notes+and+files/Aliases) (front-matter) for effecting bilingual or multilingual notes, or translation of a source-language note
- [linking to another vault](https://forum.obsidian.md/t/is-there-a-way-to-quickly-link-to-another-vault/20652) `[text](obsidian://vault/<name-of-vault>)` instead of https://
	- Or to a note: `[text](obsidian://vault/<name-of-vault>/<name-of-note-w-space-written-as-%20>)`
- block reference (>)
- swapping line up and down (cmd+1, cmd+2)
- Folding/unfolding (cmd+3)
