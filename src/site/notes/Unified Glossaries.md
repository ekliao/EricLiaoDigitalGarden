---
{"dg-publish":true,"permalink":"/unified-glossaries/","noteIcon":"2","created":"","updated":""}
---

# Desperate for a system of unified glossaries

![../_attachments/Screen Shot 2023-06-11 at 14.23.36.png](/img/user/_attachments/Screen%20Shot%202023-06-11%20at%2014.23.36.png)

This [[Anki\|Anki]] screenshot explains my plight of "glossary data duplication," specifically in headwords, better than a thousand words can.

Take the word "petition." it has 35 notes or entries in Anki. It appears in the headword field in various forms:
- Prefixed with \#, or not
- Capitalized, or not
- Singular, or plural
- ALLCAP, or not (luckily, no ALLCAP in this case)

The 35 entries were added at various times from myriad sources, over the last 3.5 years.

Anki has a "design flaw" in my opinion in that it offers only two modes of import in the case the headword entry is found to be existing in the same target deck:
1. Import anyway, resulting in duplicated headword
2. Replace the existing entry's content with the new import entry's content

The second option is a no-no. It's designed only for a specific use case: when one knows the import is a revised version that is meant to replace or update the existing deck. But this is not my scenario. My use is one of accumulation. I add new materials but keep the old. When I want to revise, I have a special routine.

So, I had to go with the first option, and over the years, this results in the 35 entries for "petition" as shown.

The pros and cons of the duplicated headword approach.

### Pros
- Data separation
- Each entry signifies a single source, and its content is coherent in the sense that it is all from the same source.
- Entries are shorter on average.
- Targeted search by `deck` is possible to pinpoint a source.

### Cons
- Number of entries blows up over time and may exceed the limit of new exchange systems, such as [[Obsidian\|Obsidian]], whose performance degrades as notes number in the 10K-100K range. (In contrast, Anki operates easily with a slight performance hit with 100K even 1M notes.)
- Extra manual actions (keyboard or mouse) are required to navigate all entries in order to view the entirety of each entry. The browser view shown here shows only the limited beginning portion of each note.
- There is little to no connection/link between these entries except by them being grouped together by an advanced search, such as `front:re:^#?petitions?$` in this case. Anki doesn't have internal links that are so naturally for Obsidian. The result is disconnected thought, not contributing to [[10 dailynotes/2023-05-26\|developing systemic thinking for interpreters]] for the meaning of "petition," combining its legal and non-legal senses, for instance.

# Unified Glossary
{ #2547bc}


What I prefer now is something that looks like this, merging all related entries of "petition" into just a single Obsidian note named "petition.md", whose content is a concatenation of all 35 entries for "petition," each preserving its original headword and metadata (source):

![../_attachments/Screen Shot 2023-06-11 at 15.01.35.png|250](/img/user/_attachments/Screen%20Shot%202023-06-11%20at%2015.01.35.png)

All future additions from new sources of "petition" will also be merged with or tacked onto the same note. Future search for "petition" will find exactly one note, and all 35 different definitions or contexts can be viewed at once with some scrolling. The unified view naturally promotes linking of different scenarios and contexts, including legal and non-legal uses. 

## Cons

- Search by specific source has to become more creative and less precise, for example, using proximity search, if available (it is, in [[DEVONthink\|DevonTHINK]]), or the `line:` operator in Obsidian.

`line: (petition src: DOJ::combine)` 

- Some automatic process needs to be created for adding new sources, such as a Python/Perl script. This is a bigger undertaking. But I believe I'll reap the rewards many times over after an initial effort of developing this process.
