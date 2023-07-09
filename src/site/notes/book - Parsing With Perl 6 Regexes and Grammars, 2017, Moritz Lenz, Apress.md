---
{"dg-publish":true,"permalink":"/book-parsing-with-perl-6-regexes-and-grammars-2017-moritz-lenz-apress/","noteIcon":"2","created":"","updated":""}
---

This book is awesome despite the errors I spotted. I have read it almost from cover to cover. It's hard, because parsing requires hierarchical thinking. Translate that into code and it's a recipe for confusion.

The part where one learns about whitespace handling and the differences between `regex`, `token`, and `rule` is especially confusing. 

## Errata

* *(2023-07-09)* The following factual errors are very unfortunate when I am trying to unravel this whitespace tangle. 

If the predefined `<ws>` construct is equivalent in code as
```
regex ws { <!ww> \s*}
```
then clearly it matches **zero to many** different whitespace characters unless it's **within a word**. The two fatal errors are: =="at least one"== and =="unless it's at a word boundary"==.

![_attachments/s an example, these two SQL statements produce identical parse.png|500](/img/user/_attachments/s%20an%20example,%20these%20two%20SQL%20statements%20produce%20identical%20parse.png)