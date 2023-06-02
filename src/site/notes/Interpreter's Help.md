---
{"dg-publish":true,"permalink":"/interpreter-s-help/","noteIcon":"2","created":"","updated":""}
---

This is one of my [[Glossary Lookup\|candidates]] for being the permanent, one-and-only glossary lookup tool. I have an account from to educator status. More reason to take advantage of it. Interpreter's Help (henceforth IH for short) is the closest among the candidates to InterpretBank, so both get extra consideration for having design facilitating the ease of quick lookup and sharing.

# Deal Breaker

- Currently (2023-05-17) search using Chinese characters doesn't work in the global search interface combining all glossaries (but work in single glossary). I've contacted the creator of IH months ago, who confirmed he could duplicate the issue I reported. As he was working on a new version, he said the defect will be fixed in the new release.
{ #a9608c}

- Update (2023-06-01): I was privy to early internal testing for the next version. Happy to report that the Chinese character search issue is fixed, for single glossary search as well as "database" search (equivalent to searching all glossaries). 

# Pros
- As one enters the search string, the search begins (i.e. is dynamic) showing the results reflecting the search string at the moment, and the result view changes as one changes the search string (usually by typing more letters or characters). This is a really good HMI (human-machine interface/interaction) design feature.

# Cons
- Each glossary is capped at 3,000 entries. Not a showstopper, just inconvenient.
- No "disappearing search string" after a preset X seconds. This is a feature in the live booth mode of [[InterpretBank\|InterpretBank]] and it gives that extra help to interpreters under stress in the booth. I suggested to the owner of IH to implement the same, calling this low-hanging fruit of a feature, something he would be able to implement in a few lines of code, considering that IH already has the dynamic search described above.

# Other features

- (Manual) terminology extractor (interface)
	- Defaults to two languages
	- Supports multiple-column as an alternative
	- Copy bilingual texts into the interface
	- The texts are secured, not stored in tool's cloud
	- Repeat:
		- Manually select terms on both side, edit if necessary, and "Add" into the glossary
	- Click "Merge lines into glossary" to produce the final glossary