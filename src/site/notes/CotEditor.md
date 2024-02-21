---
{"dg-publish":true,"permalink":"/cot-editor/","noteIcon":"2"}
---

The [[Regex 正規表式\|Regex 正規表式]] used is CUI regular expression engine ([Important changes on CotEditor 4.2 - CotEditor](https://coteditor.com/news/2022/CotEditor_4.2.0). Never heard of it. 

# Quick verdict: 3.5 stars

## Pros

- Rare treasure: amazed to discover support for `\p{Han}`, `\p{P}`, and the like. 

## Cons

- Large files: Freezes or crashes, or grinds to a halt, when opening large text files (~ > 100MB), something [[EmEditor\|EmEditor]] would handle with grace and ease. Even [Sublime Text](https://www.sublimetext.com/) (Mac) will do.
- Can't handle deleting duplicates in 800K-line files. Can't hold a candle to [[EmEditor\|EmEditor]]
	
<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/em-editor/#9a79d5" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



I have renewed unmitigated respect for EmEditor, a powerful editor that handles large text files with ease and grace. I am talking about a 500MB text file with 3.2 million lines and it still sorted it and deleted duplicates in it in a few seconds. In comparison, [[CotEditor\|CotEditor]] on Mac, despite my delight in discovering its support for Unicode script/code block regex like `\p{Han}`, can't even handle one quarter of that (800K lines) without hanging indefinitely. It's such a pity that EmEditor, my favorite text editor bar none since I found it in 2000s, is Windows-only. 

</div></div>


- [No plan](https://share.glasp.co/qke5s3ilkchdj7ts/?p=lRrPZIZl2Azx6Q6LHuUG) to support search and replace in opened files or in multiple files under a directory, not to mention recursively.
	- 
<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/regex-conditionals/#75709c" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



(Also, I hereby confirm that unfortunately [[CotEditor\|CotEditor]] does not support regex conditionals.)  

</div></div>


- [[Character class subtraction (regex)\|Character class subtraction (regex)]] is not available.
