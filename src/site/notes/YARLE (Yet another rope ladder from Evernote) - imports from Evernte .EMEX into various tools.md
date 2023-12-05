---
{"dg-publish":true,"permalink":"/yarle-yet-another-rope-ladder-from-evernote-imports-from-evernte-emex-into-various-tools/","noteIcon":"2"}
---

# From ENEX to various targets

- Obsidian
- LogSeq
- Heptabase
- Tana internal format
- Other standard markdown-based apps

![_attachments/Screenshot 2023-12-05 at 10.55.58.png](/img/user/_attachments/Screenshot%202023-12-05%20at%2010.55.58.png)

# Observation

## How it handles attachments (pictures, etc.)

After export, a `_resources` folder is created with lots of individual folders named after the notes' titles, which in turn contain the ultimate pictures. It's really complicated. In the .md file referring to a picture, there's a link reference using relative path `./_resources/`. It just works. Make sure to place .md files and the `_resources` subfolder always in the same relative positions with each other.