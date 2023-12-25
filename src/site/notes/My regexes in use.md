---
{"dg-publish":true,"permalink":"/my-regexes-in-use/","noteIcon":"2"}
---

date-created:: 2023-05-05

Here is a list of quickly-hacked-together regex patterns to mitigate tasks that otherwise seem Herculean.

## Subtitler (app) subtitle file .srt output

Search for (in CotEditor)
`^\{.*"([^\}]+)"\}\n`
Peplace with
`$1\n`
### Example

![Screenshot 2023-12-17 at 14.37.19.png|500](/img/user/Screenshot%202023-12-17%20at%2014.37.19.png)

![Screenshot 2023-12-17 at 14.37.50.png|250](/img/user/Screenshot%202023-12-17%20at%2014.37.50.png)
## In Obsidian

- Find all newly created dictionary entries with tag #td and file path not already under /A/A-Dict/(word).md

`#todo/file/d path:/[^t]\/[^\/]+\.md`
(Not robust but largely gets the job done)

- Mostly my own [[Note on the SAMPA phonetic transcription｜SAMPA音標說明\|SAMPA]] phonetic transcriptions in the form of `/.../`. Can contain non-SAMPA transcriptions of a myriad of systems from external sources, mostly dictionaries.

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
## Outside Obsidian

- Too numerous to enumerate...