---
{"dg-publish":true,"permalink":"/anki-text-tsv-import-one-huge-surprise/","noteIcon":"2","created":"","updated":""}
---

# A huge time sink: changing notetype of multiple decks

Beware! Although Anki has the option of recording the deck name in the export, allowing you to export the entire collection into one TXT (TSV) file, it does not allow you to perform the reverse action of importing this very TXT file with multiple decks in it back into Anki! This can be a nasty surprise if you aren't prepared for this. It forces you to choose one and only one existing deck name to import into, regardless of whether the import file contain the deck column or not. If it does, the deck column is IGNORED silently; ***it has zero effect.*** I feel positively duped. 😡

As shown, choosing "Notetype and deck" as Match scope (instead of just "Notetype") does not work as it leads you to believe what will happen. It still imports all content into the specified single deck (A::A-Dict in this example). 

![_attachments/Screen Shot 2023-08-19 at 12.53.06.png](/img/user/_attachments/Screen%20Shot%202023-08-19%20at%2012.53.06.png)

# More ...

[[Anki Export Considerations： text vs apkg\|Anki Export Considerations： text vs apkg]]

[[Anki - steps for bulk changing notetypes for multiple decks\|Anki - steps for bulk changing notetypes for multiple decks]]