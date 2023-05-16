---
{"dg-publish":true,"permalink":"/anki-export-considerations-text-vs-apkg/","noteIcon":"2","created":"","updated":""}
---

#Anki 
#meta/ob 

Pros and cons of these two basic ways of export, especially for:

- keeping deck name
- showing tags in content/back side (for interoperability esp. for OB)
- beware: tricky points on csv/tsv double-quote issues for text export

#regex #csv 

# Donts
- Export into cards
	- No tags
	- No deck names

# Best Choice
- Export into notes (text)
	- choose include deck names
	- choose html
	- choose tags
	- optional “unique identifier” — usually don't want this

# Text export
- Tab-separated values
- Has double quotes where they are not needed, e.g.
	`"#automatism"`
	contains no spaces nor embedded double quotes
- Embedded double quotes are shown as two consecutive double quotes, e.g. 
	`"/O ""tQ m@/"` 
	contains `/O "tQ m@"` SAMPA for “automatism”
- Backslash (\) is not escaped. 
- Commas are not the delimiter, so they are simple and not escaped or surrounded by double quotes, e.g.
	`（法律）正式書面文書 a writing that formally expresses some legal agreement, such as a contract, lease, will, deed, or bond.`
