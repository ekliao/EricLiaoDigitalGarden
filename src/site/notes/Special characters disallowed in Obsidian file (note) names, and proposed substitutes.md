---
{"dg-publish":true,"permalink":"/special-characters-disallowed-in-obsidian-file-note-names-and-proposed-substitutes/","noteIcon":"2"}
---

#meta/ob 

## Banned characters
{ #ef13b5}


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
{ #aa6d6c}


## Exceptions

Note that while the pound sign (\#) cannot be manually used in creating a new note, it can exist in the name of files that are copied under the Obsidian vault externally in the file system, e.g. 

![[../../../_attachments/Screen Shot 2023-06-08 at 15.59.07.png\|500]]

This (#) sign, however, will not be recognized as a tag.

#paste/b
### Use case or problem

Often times I want to name note files with characters that are not allowed in obsidian file names, such as /, <, >, etc.

### [Proposed solution](https://forum.obsidian.md/t/automatically-replace-unallowed-filename-characters-with-similar-special-characters/48182#proposed-solution-2)

It would be great if obsidian had the option to automatically replace these disallowed characters with HTML character look-alikes (perhaps while automatically placing the intended name with the original disallowed character(s) as an alias in frontmatter). There can be some default replacement characters in place with the option for obsidian users to use different replacement characters if they want. Here are some of my thoughts on which characters can potentially work as replacement characters:

```
/ → ⧸ (Big Solidus)  
> → ＞  
< → ＜  
: → ։  
| → ┃  
\ → ⧵  
^ → ⌃  
" → ” (closing)  
* → ＊  
[ → ［  
] → ］  
# → ⋕
```

### [Current workaround](https://forum.obsidian.md/t/automatically-replace-unallowed-filename-characters-with-similar-special-characters/48182#current-workaround-3)

Currently, I manually use the look-alike characters in the file names when needed, but this can get tedious. I also manually write the intended file name with the unallowed characters as an alias in frontmatter.
#paste/e
