---
{"dg-publish":true,"permalink":"/obsidian-pdf-plugin-demo-pdf-annotator/","noteIcon":"2"}
---

# Oh, I love this! 一見鍾情

1. Select some text in the PDF.
2. Click on a color on the toolbar. This creates a link.
3. Paste into any note. Remember to press RETURN. Voila! See the pasted result become a nice color box.
4. Hover over a link to get a popup preview of the context.

![Screenshot 2024-04-12 at 4.06.00 PM.png](/img/user/_attachments/_OB/Screenshot%202024-04-12%20at%204.06.00%20PM.png)

---
# Quick verdict: 4/5

## Cons

### Does not work with:
##### OCRed PDF book with vertical text e.g. Chinese: a huge disappointment

The performance there is much worse than [[Obsidian plugin - Annotator｜PDF註記插件\|Obsidian plugin - Annotator｜PDF註記插件]]. It's practically unusable.

One more proof: [[Notes (PDF++) - Grammaire du français (sorbonne) - 法文文法快易通 修訂版 fr-tc (ocr).pdf\|Notes (PDF++) - Grammaire du français (sorbonne) - 法文文法快易通 修訂版 fr-tc (ocr).pdf]]

---
# Issues

### 20250101 ⛔️ [[Obsidian PDF++ plugin destroys a PDF file on iPad\|Destroys a PDF file on iPad]]

### Mouse selection sticky

On one occasion, my mouse selection goes berserk: it slips and ends up selecting more text than intended as I navigate the context menu.
#### Solution

Restarting the computer worked. Glad it's only a one-off anomaly.
### 20240412 ⛔️ [[Obsidian PDF++ plugin - Auto-paste needs extra new line at the end to avoid gluing together successive quotes\|Auto-paste needs extra new line at the end to avoid gluing together successive quotes]]

---

# External PDF

#gpt 
In Obsidian, the "PDF++" plugin allows you to link to external PDF files by simply ==dragging and dropping the PDF file directly into your Obsidian note==, which creates a link to the file's location on your computer; essentially treating the PDF as an attachment, even if it's not physically stored within your Obsidian vault folder, enabling you to access it through the link within your note. 
#pplx 
在 Obsidian 中，「PDF++」外掛允許您通過直接將 PDF 文件拖放到您的 Obsidian 筆記中來鏈接外部 PDF 文件，這會自動建立一個指向該文件在您電腦上位置的連結；本質上將 PDF 視為附件，即使它並未實際存儲在您的 Obsidian Vault 資料夾內，也能讓您通過筆記中的連結訪問該文件。

Key points about linking external PDFs with PDF++:
關於使用 PDF++ 鏈接外部 PDF 的重點：

Drag and drop functionality:
The most common method is to drag a PDF file from your file explorer and drop it into your Obsidian note, automatically generating a link to that file.

拖放功能：
最常見的方法是從檔案總管中拖動 PDF 文件並將其放入您的 Obsidian 筆記中，系統會自動生成指向該文件的連結。

External file location:
The link will point to the actual location of the PDF file on your computer, not necessarily within your Obsidian vault. 

外部文件位置：
該連結會指向您電腦上 PDF 文件的實際位置，而不一定需要位於您的 Obsidian Vault 資料夾內。

Opening the PDF:
When you click on the link in your Obsidian note, the default PDF viewer on your system will open the external file.

開啟 PDF：
當您點擊 Obsidian 筆記中的連結時，系統預設的 PDF 檢視器會自動打開該外部文件。

---
# More ...

[[Combining PDF reading, annotating, backlinking for context, and flashcarding 一邊閱讀筆記一遍建立閃卡\|Combining PDF reading, annotating, backlinking for context, and flashcarding 一邊閱讀筆記一遍建立閃卡]]

[[Obsidian plugin - Annotator｜PDF註記插件\|Obsidian plugin - Annotator｜PDF註記插件]]

[[PDF annotation - non-OCR PDF - text selection woes\|PDF annotation - non-OCR PDF - text selection woes]]

- Explains options, including caution against "enable PDF editing" (which I turned ON)
https://pkmer.cn/Pkmer-Docs/10-obsidian/obsidian%E7%A4%BE%E5%8C%BA%E6%8F%92%E4%BB%B6/pdf-plus/

- Introduces Markmind plugin #todo/try #Obsidian/plugin 
https://zhuanlan.zhihu.com/p/438755703
- [obsidian markmind 插件](https://link.zhihu.com/?target=https%3A//www.markmind.net/cn)已经实现在 ob 中阅读标注 pdf, 具有形成思维导图, pdf 跳转的功能; 该插件配置, 在 markmind 的基础上, 结合 quickadd 和 Templater 插件, 进一步对 pdf 标注进行操作, 实现每条 pdf注释 单独生成一个文稿, 并手动打上标签, 方便日后归纳整理检索分类**