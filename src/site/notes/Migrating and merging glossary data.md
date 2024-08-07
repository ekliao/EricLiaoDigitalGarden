---
{"dg-publish":true,"permalink":"/migrating-and-merging-glossary-data/","noteIcon":"2"}
---

# The Problem

Over the last three years, I have added some 1.2 million entries of glossary and dictionary-like data to Anki. The predominant mode of accumulation is allowing duplicate headword fields. For example, the headword `reasonable doubt` may have 20 entries from various decks, some obviously for legal glossaries, others general. Of the 1.2 million entries, there may only be 400K unique headword fields.
{ #3f8140}


At one point, I pondered about merging all entries sharing the same headword into one entry, to eliminate Anki's overhead for large number of notes and to make browsing the search results more convenient, requiring few mouse clicks. The advantage for the merged approach was most obvious in dealing with a massive collection of dictionaries and technical glossaries. I have such a set with probably more than 3 million entries (including duplicated headwords). For instance, the simple headword `set` is found in 40 entries, each from a dictionary or a special glossary. It would be beneficial to merge all `set` entries into one, and allow subentries to show their source, data, metadata, etc., to preserve separability for the future.

Since I built a new core glossary vault in Obsidian, this need for merging duplicates has become urgent, as Obsidian becomes sluggish and slow searching 50K notes, let alone 300K or 3 million!

The better-looking markdown presentation of OB also make reading a large merged note for, say, `set`, containing 40 data sources, much more pleasant. Being able to see in one place all the different definitions, translations, and contexts for `set` is extremely hopeful for gaining insight and knowledge about a term. This knowledge-from-proximity is hard to come by if I have to manually click through 40 notes.

So, I would like to start a short-term programming project for coming up with code (in Perl or Python) that will deal with merging data to reduce the total number of entries.

One key issue is normalizing the headword entry before determining whether A and B belong in the same final entry. I should design and describe the normalization carefully so that it makes intuitive sense for the purpose of glossary lookup.


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/special-characters-disallowed-in-obsidian-file-note-names-and-proposed-substitutes/#aa6d6c" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



```
/ → ⧸ (Big Solidus)  【巜full-width slash cannot be typed for some reason by Rime/Squirrel 】
: → ։ OR full-width ： 
[ → { OR full-width ［  
] → }  OR full-width ］ 
# → ⋕ OR full-width 
< → ＜  OR full-width 〈
> → ＞  OR full-width 〉
| → ┃  OR fulld-width ｜
" → “ OR ”  
* → ＊ (same as full-width ＊ ?) 
^ → ⌃  【巜can't type full-width】
\ → ⧵  OR full-width ＼ 
```

</div></div>


For each of the banned characters in OB note name, there should be a rule for normalizing it. But I should consider all non-alphanumeric symbols together, adding the following:

```
[all whitespace characters]
(
)
（ [full width]
） [full width]
{
}
「
」
【
】
〔
〕
［ [full width]
］ [full width]
' 
‘’ [a pair: opening and closing]
- [hyphen]
— [both em- and en-dash]
_ [underscore]
; [and full width]
! [and full width]
? [and full width]
， [full width]
.
。 [full width]
@
$
%
&
+
=
```

---

# Related
- [[Special characters disallowed in Obsidian file (note) names, and proposed substitutes\|Special characters disallowed in Obsidian file (note) names, and proposed substitutes]]
- [[Unified Glossaries\|Unified Glossaries]]