---
{"dg-publish":true,"permalink":"/google-sheets-regex-find-and-replace/","noteIcon":"2"}
---

date-created:: 2023-08-15

#regex
Google Sheets allows regex in find and replace. This is extremely helpful in turning embedded newlines (`\n`) into HTML <br/> for CSV or TSV files for Anki. 

It's important to do this find and replace to recode newlines as HTML before downloading the file as CSV and TSV. Without this step, all those newlines will turn into simple spaces, losing their newlineness.
{ #bf6e98}

## Before
![[_attachments/Screen Shot 2023-08-15 at 22.03.27.png\|_attachments/Screen Shot 2023-08-15 at 22.03.27.png]]
## Applying regex

![[_attachments/Screen Shot 2023-08-15 at 22.04.34.png\|_attachments/Screen Shot 2023-08-15 at 22.04.34.png]]
## After

![[_attachments/Screen Shot 2023-08-15 at 22.09.08.png\|_attachments/Screen Shot 2023-08-15 at 22.09.08.png]]

