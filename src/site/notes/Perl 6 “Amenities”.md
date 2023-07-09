---
{"dg-publish":true,"permalink":"/perl-6-amenities/","noteIcon":"2","created":"","updated":""}
---

There are so many little delightful things that Perl 6 offers, so I'm gathering them into this note.

## [Predefined Regexes](https://docs.raku.org/language/regexes#Predefined_Regexes)

|Regex|Zero-width|Matches|
|---|---|---|
|\<same>|yes|Matches between two identical characters|
|\<wb>|yes|Word boundary|
|\<ws>|no|Whitespace, same as: `<!ww>\s*`|
|\<ww>|yes|Within word|
|\<ident>|no|Basic identifier (no support for ' or -). Same as: `<.alpha> \w*`|
