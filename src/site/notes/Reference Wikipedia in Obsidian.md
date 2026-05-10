---
{"dg-publish":true,"permalink":"/reference-wikipedia-in-obsidian/","noteIcon":"2","dg-note-properties":{}}
---

# Hotkeys

Three are currently set.

![Screen Shot 2023-05-09 at 10.55.29.png](/img/user/_attachments/_OB/Screen%20Shot%202023-05-09%20at%2010.55.29.png)

# Quick verdict
None are perfect. I prefer #2, but it doesn't work for anything but English except the language is force changed (see 2a below). 🤷

---
## 1. Insert Link Text and Link
- Works for any language
	- Prefix `zh:` `fr:`, default `en:`

#resultof/command Wikipedia Search: Search Article > menu > enter `zh:唐裝`

[唐裝](https://zh.wikipedia.org/wiki/%E5%94%90%E8%A3%9D)

## 2. Insert the first paragraph for the search term
- English only
- Note that the first word repeats the search term `tangzhuang`, in lowercase, followed by `>` and then the actual Wikipedia, unbolded.

#resultof/command get wikipedia for search term > menu > enter `tangzhuang`

tangzhuang> Tangzhuang (Chinese: 唐裝; pinyin: Tángzhuāng; lit. 'Chinese suit'), sometimes called Tang suit,: 50  is a kind of Chinese jacket with Manchu origins and Han influences, characterized with a mandarin collar closing at the front with frog buttons. It is an updated form of the Qing magua, itself a more fashionable adaptation of the riding jacket once worn by Manchu horsemen. Nowadays, the tangzhuang is one of the main formal clothing worn by Chinese men on various occasions; overseas Chinese also wear it as a form of fashion or to express their cultural identity.: 191
>
> [Wikipedia](https://en.wikipedia.org/wiki/Tangzhuang)

### 2a. Insert the first paragraph for the search term
- *(Onetime) force change the community plugin `(Obsidian) Wikipedia` settings to use `zh` language prefix (default is `en`)
- Note that the quoted result is always the default in Simplified Chinese (唐装...) despite the search term being Traditional Chinese `唐裝`. At least, using TC search term works.
- Despite the now `zh` setting, the #1 method `ctrl-shift-W` search can still use `en:` to find English articles, and insert the link. All is not lost.
 
![Screen Shot 2023-05-09 at 11.18.52.png\|600](/img/user/_attachments/_OB/Screen%20Shot%202023-05-09%20at%2011.18.52.png)

#resultof/command get wikipedia for search term > menu > enter `唐裝`

> 唐装，台灣又稱漢衫、唐山衫，是清代至現代华人的一種傳統服飾。特点是立领及盘扣，1950年代之後，一些**唐裝**又吸收了一些西式裁剪的特点，例如立體剪裁、在肩膀部接袖等。港澳、台灣所指的唐裝包括男裝的長衫，男女通用的對襟衫、大襟衫等等。
>
> [Wikipedia](https://zh.wikipedia.org/wiki/%E5%94%90%E8%A3%85)

## 3. Insert the first paragraph for the current note title
- English only
- Same as #2 above except the exact casing of the note title is used, without the actual Wikipedia title. Compare the following two, where the difference is in the casing of the note's title.

#resultof/command get wikipedia for active note title `Tangzhuang`

> **Tangzhuang** (Chinese: 唐裝; pinyin: Tángzhuāng; lit. 'Chinese suit'), sometimes called Tang suit,: 50  is a kind of Chinese jacket with Manchu origins and Han influences, characterized with a mandarin collar closing at the front with frog buttons. It is an updated form of the Qing magua, itself a more fashionable adaptation of the riding jacket once worn by Manchu horsemen. Nowadays, the tangzhuang is one of the main formal clothing worn by Chinese men on various occasions; overseas Chinese also wear it as a form of fashion or to express their cultural identity.: 191
>
> [Wikipedia](https://en.wikipedia.org/wiki/Tangzhuang)

#resultof/command get wikipedia for active note title `tangzhuang`

> **tangzhuang** (Chinese: 唐裝; pinyin: Tángzhuāng; lit. 'Chinese suit'), sometimes called Tang suit,: 50  is a kind of Chinese jacket with Manchu origins and Han influences, characterized with a mandarin collar closing at the front with frog buttons. It is an updated form of the Qing magua, itself a more fashionable adaptation of the riding jacket once worn by Manchu horsemen. Nowadays, the tangzhuang is one of the main formal clothing worn by Chinese men on various occasions; overseas Chinese also wear it as a form of fashion or to express their cultural identity.: 191
>
> [Wikipedia](https://en.wikipedia.org/wiki/Tangzhuang)





---

