---
{"dg-publish":true,"permalink":"/easy-find/","noteIcon":"2"}
---

## Pros
- Free
- [[Regex 正規表式\|Regex 正規表式]] search of file names and content
- 
## Cons
- A query can't operate on BOTH file names and content. Only one.

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/10-dailynotes/2023-04-24/#a2e99b" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



- To my disappointment, [[EasyFind\|EasyFind]] does not reliably find text in files as expected. I tried to look for a simple fixed string such as `disqus` in a directory tree of files and it found fewer files than expected. I have no idea why such a simple search failed. In comparison, the tried-and-true [[Text Editors#^81cbb4\|EmEditor]] (available on Windows only, alas) did fine. 

</div></div>


## Verdict: 4 stars
- Use it mainly for quick search of files by name. 
- Can be convenient for regex search inside files (see Hacks below).

---
## Hacks

- *(2023-07-13)* Selecting all and moving those resulting files in one go into a single target directory can be done. Slow but possible (see video below). This trick can be handy.
	- e.g. In the video, I search for `#md\b` and moving found files from at least two different folders en masse into one single target. Took 2 tries.

![[_attachments/easyfind - moving files from different source directories into one target directory - possible but slow, may need several tries.mp4]]