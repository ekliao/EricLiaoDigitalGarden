---
{"dg-publish":true,"permalink":"/my-first-non-hello-world-perl-6-program/","noteIcon":"2","created":"","updated":""}
---

#Perl6
```
To exit type 'exit' or '^D'
[0] > for '/usr/share/dict/words'.IO.lines -> $word {
* say $word if lc($word) ~~ /^ .e.rl $/;
* }
ceorl
pearl
[0] > 
```
In just two lines of code, it does something that would have taken like 15 lines in Python and 100 lines in Java in my guesstimation.
