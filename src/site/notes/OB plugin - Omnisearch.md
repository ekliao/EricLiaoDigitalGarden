---
{"dg-publish":true,"permalink":"/ob-plugin-omnisearch/","noteIcon":"2","created":"","updated":""}
---

Any functionality offering full-text indexing and search get my attention. This one for the OB vault definitely sounds awesome at first sight.

#rating 
### Quick verdict: 2 stars

The underscoring search terms in in the results is nice. Looks like multiple search terms separated by spaces mean the `AND` operator: all of these terms, a typical “idiom.”

## History

- *(2023-05-04)* Tends to crash the iOS mobile version. Disabled it there.

- *(2023-05-04)* On the first use I found a bug immediately:

![Screen Shot 2023-05-04 at 11.43.14.png](/img/user/_attachments/Screen%20Shot%202023-05-04%20at%2011.43.14.png)

As show, it treats `interpret` and `internet` as words with the same lemma through an obviously crude and dumb process of lemmatization.

To its defense, many tools out there, such as [[Cymo Note\|Cymo Note]], a CAI tool that I was interested enough to check out, don't even do any lemmatization but use the basest form of search: strict whole-string matching. Compared with them, some lemmatization is still a welcome effort.
