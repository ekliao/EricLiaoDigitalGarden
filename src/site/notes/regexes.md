---
{"dg-publish":true,"permalink":"/regexes/","noteIcon":"2","created":"","updated":""}
---

A list of quickly-hacked-together regex patterns to mitigate tasks that otherwise seem Herculean.

## In OB

- Mostly my own [[Note on the SAMPA phonetic transcription\|SAMPA]] phonetic transcriptions in the form of `/.../`. Can contain non-SAMPA transcriptions of a myriad of systems from external sources, mostly dictionaries.

`/[^a-z0-9\/]\/[^\/024-9]{1,20}\/[^a-z\)]/`

e.g. 

*(annotation in parentheses: /SAMPA/ but \[IPA\])*

SAMPA: ==/"e1 oU "ke1/== 
non-SAMPA: 
	IPA *(mwald)* ==/ˌeıoʊˈkeı/==
	IPA-variant *(node)*
		==/ ˈeiˈwʌn /== (\[i\] for \[ı\])
		==/ ˈæblaut /== (/u/ for /U/)

- M-w style transcriptions in the form of `\ ... \`.

`/\\\\ [^\\]{1,100}[ˌˈ].[^\\]{1,100}\\\\/`

e.g. ==\\ si-​ˈkwe-​(ˌ)lē\\==

- Other sources using the square brackets: `[...]`
#todo 

---
## Outside OB
