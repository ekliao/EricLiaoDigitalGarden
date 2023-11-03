---
{"dg-publish":true,"permalink":"/notion/","noteIcon":"2"}
---

date-created:: 2023-08-12

I have said a few times that Notion looked like overkill compared with [[Obsidian\|Obsidian]]. I now admit that it was out of my ignorance: I didn't know how to make of Notion as it looked alien at a time before I came to learn about block-based or database-like PKM systems.
# Hello, Notion!

My first distrust and distaste of Notion came a few weeks ago when it simply failed to delivery by bluntly showing this "Import failed" message without any explanation:

![_attachments/useless Notion CSV import error message.png|400](/img/user/_attachments/useless%20Notion%20CSV%20import%20error%20message.png)

I chose to import a CSV file that I converted using Google Sheets from an Anki TSV. 

On several other occasions, Notion was stuck with importing (having accepted the import file at 100%) for hours (close to 24 hours). Another sign telling me the tool's design was seriously flawed.

I thought I was going to leave it for good, ready to chalk it as a completely overhyped, unusable tool.

Then, after trials and tribulations with Logseq, Tana, and recently with a new surprise from Anki, I chanced upon the cause of import failure: Notion "capriciously" gave more helpful error message:

![_attachments/helpful Notion CSV import error message.png|250](/img/user/_attachments/helpful%20Notion%20CSV%20import%20error%20message.png)

So, the failure was caused by inconsistent number of columns, which is strange coming from Anki, but I dug deeper and found why. It was due to my overly simple attempt to convert from TSV to CSV. To make a long story short, after using Sheets to read TSV, double-checking data consistency, and exporting as CSV, the CSV was magically processed by Notion, and I had my first Notion page with 3000 entries from Anki!

This was screaming-worthy. I skipped the celebratory drink (it was just 11AM) and quickly found out some pros and cons of Notion as initial impressions:
## Pros
- Neat table and multi-view design
- Benefits of everything that comes with a typical database
- Search as you type (also: filter, formula)
- Can add to the database by importing CSV with matching columns/properties
- Not too slow
## Cons
- No regex in the most needed places: search and filter.
	- Cumbersome regex in formula, as string arguments to functions.
- Search does not accept multiple words, not even English, defaulting to "AND" search, like Anki.
	- To simulate this requires constructing two filters that are ANDed.
	- It accepts only one unquoted search string as that can contain spaces, and uses it to do strict substring matching. 
# Quick verdict: 3 stars

---
# Web publishing

## Demo

### [[Fred Jame\|Fred Jame]]'s [Notion site](https://fred.mba/)
- At first sight, I actually like it a lot. #todo Dig deeper.
## Namanh Kapur
#people
- [Video that may sell me on notion!](https://www.youtube.com/watch?v=8u45QMEn1o4)
	- Reiterates why having a personal website is important
		- But having a website without good SEO is useless
- Video notes
	- Progression of building a website
		- v1: Git 2/5
		- v2: Script for Medium 3/5
		- v3: Ghost 3.5/5
			- Copy-and-paste from Medium
		- v4: Notion 4/5
			- Free
			- Templates
		- v5: super.so 4.9/5 (wrapper around Notion workspace)
			- Free!

---
# More ...

- [[Refocusing on Glossary Management\|Refocusing on Glossary Management]]