---
{"dg-publish":true,"permalink":"/obsidian-plugin-annotator-pdf/","noteIcon":"2","created":"","updated":""}
---

This seems a cool tool. I've been searching for a consistent and habit-forming way to highlight and annotate a PDF file in Obsidian.

#project/learn-by-doing 
#project/completed 
- Requires a new OB file/note pointing to the PDF (as attachment)
- Add frontmatter	
	- `annotation-target:<pdf-file-name-including-extension-dot-pdf`	
	 - [Clip](https://youtube.com/clip/Ugkxo50smJxJAAF5F-SxhnAsN2FGYklE5D0i)
Or: in-line video:
![[what to do after creating annotation-target frontmatter for a new note.mp4]]
[src](https://www.youtube.com/watch?v=lISOJeu7fgU&t=326s)
- Can switch between three views (click `Show Annotation` in markdown view to go back to the PDf view)
	- Default annotation view (reading, highlighting and annotating it, with an annotation pane on the right and a outline pane on the left)
	- Markdown view (with lots of metadata, code, and the actual textual annotation, which can be searched). ==Keep this view read-only. See Pitfalls below==.
	- Reading mode of this markdown (nice!)

### Pitfalls
- (2023-05-08) Though tempting, don't ever ==edit the textual annotation directly in the markdown view==. It will cause the annotation view to not show properly!

# Pic or it didn't happen

Lo and behold!

![Screen Shot 2023-05-08 at 11.57.50.png](/img/user/_attachments/Screen%20Shot%202023-05-08%20at%2011.57.50.png)

---
# Pros

## Textual annotations are searchable in OB's general search, and lead to original doc and annotation

![_attachments/Screen Shot 2023-05-21 at 14.13.23.png](/img/user/_attachments/Screen%20Shot%202023-05-21%20at%2014.13.23.png)

# Cons

## No free-form hand-drawing or underlining, only highlighter and textual comments
😭 No free-form hand-drawn annotation! Look at this page, made with the Apple Pencil on a screenshot on the iPad. This is what I need, to be able to draw lines and circles to help make my point.

![IMG_6A993934BA76-1.jpeg](/img/user/_attachments/IMG_6A993934BA76-1.jpeg)

## Annotation pane search does not work

The search on the annotation pane does not work, e.g. `solutions` should find the specific annotation that says "solutions inside". This works, however, on the left-nav general search for all files. Even though it is findable, locating the found annotation from the left-nav result is a pain, because clicking on the result doesn't home in on the target.
![_attachments/Screen Shot 2023-05-19 at 21.06.48.png](/img/user/_attachments/Screen%20Shot%202023-05-19%20at%2021.06.48.png)

## iPad usability

### Good luck on getting Obsidian iPad (or iOS) to work

(2023-10-01) I've given up on this. The hell of infinite sync of configuration is real. See  
<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/obsidian-issues/#i-cloud-free-sync-is-often-stuck-in-synchronizing-the-obsidian-configuration-files" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



### iCloud free sync is often stuck in synchronizing the Obsidian configuration files

This view on my iPhone has become a daily eyesore:

![_attachments/IMG_EAE1F33EA278-1.jpeg|250](/img/user/_attachments/IMG_EAE1F33EA278-1.jpeg)
- [The problem, and two potential solutions using Github (manual sync) and Apple Scriptable](https://www.reddit.com/r/ObsidianMD/comments/vdal97/is_there_a_way_to_shorten_this_waiting_time_or/)

---

</div></div>

### Text selection

(2023-05-19) On the iPad, selecting a portion of text beyond one line can be very frustrating, because the screen will show the wrong selection or show highlight filling the entire screen. I had previously thought this to be tolerable, but now I have experienced this terrible problem enough that I am counting out this plugin as a be all, end all PDF reading and annotating tool for me. Despite the OB integration, this is not worth it. Use LiquidText instead. It allows free-form drawing, and that trumps anything.

# Quick verdict: 3 stars

For this reason, I ~~am reconsidering~~ decided to return to [[LiquidText\|LiquidText]] as the all-around tool for PDF note-taking.