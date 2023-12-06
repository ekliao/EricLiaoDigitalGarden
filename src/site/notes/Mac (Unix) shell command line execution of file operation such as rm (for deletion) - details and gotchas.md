---
{"dg-publish":true,"permalink":"/mac-unix-shell-command-line-execution-of-file-operation-such-as-rm-for-deletion-details-and-gotchas/","noteIcon":"2"}
---


## At command line, run:

`chmod 777 <text-batch-file-name.txt>`
`zsh <text-batch-file-name.txt>`

Key points:
- Precede the batch file name with `zsh` (the Mac shell)

## Sample lines in the batch file

`rm 魔鬼，說出你的名字，別拿下一代當擋箭牌\!\ @\ CHEER\ 痞客邦\ PIXNET.md`
`rm XX教授\ -\ 臺北市立大學－社會暨公共事務學系\ 2.md`

Key points:
- No double quotes surrounding the files to be deleted.
- Escape every non-alphanumeric characters (spaces, quotes, exclamation points, carets, at signs, backticks, etc.) with one backspace.
