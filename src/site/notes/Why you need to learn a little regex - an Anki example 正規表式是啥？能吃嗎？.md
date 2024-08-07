---
{"dg-publish":true,"permalink":"/why-you-need-to-learn-a-little-regex-an-anki-example/","noteIcon":"2"}
---

date-created:: 2023-10-16

It took me ten seconds to write the reply to help out a fellow Anki learner in the Facebook group, so it doesn't normally warrant a post, but I couldn't think of a more perfect scenario for explaining why knowing even a little regex can be a life-saver sometimes. In this case, one wants to search for a word like "lit" and does not want to see words like "little" in the search results. In other words, you would check the "whole word" or "exact" search option. But Anki does not have this option per se. This is where regex comes in. One can achieve the same purpose by using the `\b` anchor in regex:

`re:\blit\b`

`re:` is the keyword in Anki telling it what comes next is to be interpreted as regex, not to be taken literally.

雖只是舉手之勞，但這簡直是一個完美的例子，告訴你不會用 regex 只能哭天喊地。

![[_attachments/Screen Shot 2023-10-16 at 01.41.43.png\|600]]

Read more about [[Regex 正規表式\|regex]]. 多認識一點 [[Regex 正規表式\|正規表式]]。