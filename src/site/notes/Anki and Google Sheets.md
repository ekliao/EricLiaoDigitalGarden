---
{"dg-publish":true,"permalink":"/anki-and-google-sheets/","tags":["gardenEntry"],"noteIcon":"2","created":"","updated":""}
---

date-created:: 2023-08-17

Google Sheets is invaluable at processing Anki txt export especially in being able to process ***embedded newlines*** correctly in Anki's TSV output. 

Upon importing an Anki txt file, specifically choose the separator as Tab, and absolutely uncheck the ***Convert text to numbers, etc.*** checkbox. We want everything treated as plain text.

![_attachments/Screen Shot 2023-08-17 at 14.27.50.png|250](/img/user/_attachments/Screen%20Shot%202023-08-17%20at%2014.27.50.png)

As I have mentioned in a different post, before downloading the spreadsheet as TSV for importing into Anki:


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/google-sheets-regex-find-and-replace/#bf6e98" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



It's important to do this find and replace to recode newlines as HTML before downloading the file as CSV and TSV. Without this step, all those newlines will turn into simple spaces, losing their newlineness. 

</div></div>


![_attachments/Screen Shot 2023-08-15 at 22.04.34 1.png|400](/img/user/_attachments/Screen%20Shot%202023-08-15%20at%2022.04.34%201.png)