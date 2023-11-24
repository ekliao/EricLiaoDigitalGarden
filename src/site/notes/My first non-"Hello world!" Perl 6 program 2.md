---
{"dg-publish":true,"permalink":"/my-first-non-hello-world-perl-6-program-2/","noteIcon":"2"}
---

#Perl6

#### Invoking perl6 from the good ol' command line
```
ekliao@ELI-1T-Side-MBP14 ~ % perl6

Welcome to Rakudo™ v2023.06.
Implementing the Raku® Programming Language v6.d.
Built on MoarVM version 2023.06.
To exit type 'exit' or '^D'
```
#### Entering actual code here
```
[0] > for '/usr/share/dict/words'.IO.lines -> $word {
* say $word if lc($word) ~~ /^ .e.rl $/;
* }
```
#### Executing code
```
ceorl
pearl
[0] > 
```
As is its wont, in just two lines of code, Perl 6 does something that would have taken like 20 lines in Python and 100 lines in Java in my guesstimation: it takes in all words in the built-in English word file (`/usr/share/dict/words`), one per line, and prints all words that match the regex `^ .e.rl $`. Turns out there are two.

One apparent convenience Perl 6 has over Perl 5 is that the whitespace inside a regex pattern is by default ignored, to enhance readability. Another feature not illustrated here is that single-line comments (beginning with the \# character) can be embedded in regex too. I really appreciate this effort to encourage more regexing!