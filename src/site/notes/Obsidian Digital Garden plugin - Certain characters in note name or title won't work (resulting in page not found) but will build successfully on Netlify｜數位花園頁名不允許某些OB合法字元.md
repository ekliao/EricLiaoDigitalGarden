---
{"dg-publish":true,"permalink":"/obsidian-digital-garden-plugin-certain-characters-in-note-name-or-title-won-t-work-resulting-in-page-not-found-but-will-build-successfully-on-netlify-ob/","noteIcon":"2"}
---

It's annoying and surprising to find that following valid characters in the note name (file name) cannot be used for publishing. The Netlify build will work yet result in an empty page:
# Double quote (")

For example, I had a blogpost originally with "meta" in the headline/note title/note name. While Obsidian obviously accepts the double quote as a legal character, so does the MacOS file system, this post will fail to be shown on the web site with Netlify. 

![Screenshot 2024-04-10 at 2.35.24 PM.png|300](/img/user/_attachments/_OB/Screenshot%202024-04-10%20at%202.35.24%20PM.png)

==Workaround==: 

- Remove the double quotes
- Use the single quote (the apostrophe), smart quotes, or double byte quotes, etc.
---

[[Obsidian Issues 問題\|Obsidian Issues 問題]]

