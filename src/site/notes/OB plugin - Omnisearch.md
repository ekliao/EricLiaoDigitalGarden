---
{"dg-publish":true,"permalink":"/ob-plugin-omnisearch/","noteIcon":"2","created":"","updated":""}
---

The higlighting of searched terms in light-yellow underscore in the results is nice.

- *(2023-05-04)* The promise of a full-text indexing of the OB vault sounds good, but on the first use I found a bug immediately:

![Screen Shot 2023-05-04 at 11.31.00.png](/img/user/_attachments/Screen%20Shot%202023-05-04%20at%2011.31.00.png)

As show, it treats `interpret` and `internet` as words with the same lemma through an obviously crude and dumb process of lemmatization.

To its defense, many tools out there, such as [[Cymo Note\|Cymo Note]], a CAI tool that I was interested enough to check out, don't even do any lemmatization but use the basest form of search: strict whole-string matching. Compared with them, some lemmatization is still a welcome effort.