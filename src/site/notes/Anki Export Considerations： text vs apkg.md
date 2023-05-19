---
{"dg-publish":true,"permalink":"/anki-export-considerations-text-vs-apkg/","noteIcon":"2","created":"","updated":""}
---

#Anki 
#meta/ob 

Pros and cons of these two basic ways of export, especially for:

- keeping deck name
- showing tags in content/back side (for interoperability esp. for OB)
- beware: tricky points on csv/tsv double-quote issues for text export

#regex #csv #tsv

# Donts
- Export into cards
	- No tags
	- No deck names

# Best Choice
- Export into "Notes in Plain Text" with the following choices
	- include deck names
	- include html
	- include tags
	- optional “unique identifier” — usually not wanted

# Notes in Plain Text export format
- An entry per line
- Tab-separated values (fields)
- Functional HTML tags in all fields are shown as is, e.g. `<b>`.
- Header:
```
#separator:tab
#html:true
#deck column:1
#tags column:4
```
- Entries without tags will still end with a tab character.

## The tab character
- Make sure there are no literal tab characters (\\t) in the third (content) field. Protect it first before exporting, or it will be replaced with 3 consecutive `&nbsp;`. What is worse, the plain html tags (< and >) in that entry will each become `&lt;` and `&gt;`.

## The double quote
### Where a pair surrounds the entire field
- When not needed, e.g. when the content field contains no spaces nor embedded double quotes:
	`"#automatism"`
- Used to "escape" a literal double quote in text, e.g. 
	`"What is written at the top of all papers (called ""pleadings"") given to the court."` 
- Used to embed a literal newline character, e.g. after the `<div>` tag:
```
deckname[tab]front[tab]"<p>foo<p/><div>
bar</div>baz"[tab]tag1 tag2
```

### Absence
- The backslash (\\) is not escaped. 
- Commas are not the delimiter,. They are simple, not escaped nor surrounded by double quotes, e.g.
	`n. A violation of a law, obligation, or promise.`

## Non-functional HTML characters
- In the third (content) field, non-functional HTML characters (<, >, &) are shown as HTML entities, e.g. `&lt;`, `&gt;`, `&amp;`.
