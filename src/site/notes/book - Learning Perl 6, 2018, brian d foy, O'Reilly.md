---
{"dg-publish":true,"permalink":"/book-learning-perl-6-2018-brian-d-foy-o-reilly/","noteIcon":"2"}
---

While I enjoyed the famous llama book Learning Perl (for Perl 5), coauthored by brian d foy, I couldn't put my finger on why his solo work Learning Perl 6 feels off.

## Errata
* *(2023-07-09)* After spotting two bad errors regarding `<ws>` in the [[book - Parsing With Perl 6 Regexes and Grammars, 2017, Moritz Lenz, Apress\|book - Parsing With Perl 6 Regexes and Grammars, 2017, Moritz Lenz, Apress]] book, I tried to look for and expected clarity in guidance from this book. Instead, I found what appears to be more confusing errors and terribly imprecise misused language.

First, `<|wb>`, according to [official documentation](https://docs.raku.org/language/regexes#Word_boundary), is wrong. It should be

`<?wb>` or the hard-to-understand `<|w>`.

Second, the comment "required between word characters, optional otherwise" is just plain wrong. It's confusing language. A word character should be \[a-zA-Z0-9_\] or any Unicode letter. If we take "Hello world!", "between word characters" therefore would mean any point where I added a \^:

`H^e^l^l^o w^o^r^l^d!`

Those points aren't places where whitespace is required. Quite the opposite.

What the author means to say is "between words" or more verbosely, "between a word character and a non-word character." If we ignore both ends, there are exactly two points where `<ws>` can occur:

`Hello^world^!`


![[_attachments/Table 15-1. Named character classes.png\|450]]

In terms of confusing writing, seriously I'm appalled, but one instance is forgivable. Will watch out for more.