---
{"dg-publish":true,"permalink":"/chat-gpt-for-term-or-idiom-extraction/","noteIcon":"2","created":"","updated":""}
---


## Quick verdict
- ChatGPT does not do a good enough job extracting idiomatic expressions. It's 50/50, hit-and-miss. Maybe I haven't learned what the magic command should be.
- The fact that ChatGPT, being hugely skewed towards English data (what >98% of its training is based on), outputs English translation of the Chinese terms is a welcome by-product.

#ChatGPT/text 

```
Q:

List all Chinese idioms, idiomatic expressions, or typical four-character sayings in the following passage:

[See input data below]

A:

經典回眸 - classic look back
時尚寶典 - fashion bible
幸福基本 - basically all happiness
引領風向 - lead the trend
模特荒 - model shortage
秀外慧中 - beautiful outside and intelligent inside
評頭論足 - criticize and make comments
洗片房 - film developing room
意外闖進 - accidentally break into
感情移入論 - empathy theory
共鳴 - resonance
放鴿子 - stand someone up
出現在眾人面前 - appear in front of everyone
大放異彩 - shine brilliantly
潮流風向標 - trend indicator
空有皮囊 - Empty Vessel
動之以情 - Moving with Emotion
```

My critique:

Valid:
```
秀外慧中 - beautiful outside and intelligent inside
評頭論足 - criticize and make comments
放鴿子 - stand someone up
大放異彩/大放光彩 - shine brilliantly
動之以情 - Move/persuade someone with Emotion
引領潮流/引領風向 - lead the trend
空有皮囊 - Empty Vessel
時尚寶典 - fashion bible
```

Invalid:
```
經典回眸 - classic look back
時尚寶典 - fashion bible
幸福基本 - basically all happiness
洗片房 - film developing room
意外闖進 - accidentally break into
感情移入論 - empathy theory
共鳴 - resonance
出現在眾人面前 - appear in front of everyone
潮流風向標 - trend indicator
```

Missing:
```
浩浩蕩蕩 - in a grand and imposing manner or in a majestic and vigorous way
一籌莫展 - at a loss; unable to come up with a plan or solution 
曉之以理 - enlighten with reason
一門心思 - single-minded; wholeheartedly devoted to something; have one's mind set on something
心懷不軌 - have evil intentions or have nefarious intentions.
落湯雞 - drenched and bedraggled, like a drowned rat, deep distress
不為所動 - unmoved or unswayed
翩翩起舞 - dancing lightly and gracefully

```

Input: results from this:

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/chat-gpt-conversion-from-simplified-chinese-writing-to-traditional-chinese-for-taiwan/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




with special instructions on wording differences

## Instructions
#ChatGPT/text 
```
Q: Convert the following Chinese into Traditional Chinese for Taiwan, paying attention to differences in wording and usage:
```
A: 
![[chatgpt converting sc to tc w instruction on wording differences.html]]

Of the differences in the result, these are valid conversions:
- 徑自 -> 直接
- 一門心思 -> 一心一意
- 酒店 -> 飯店
- 模特 -> 模特兒

Original text for conversion:

```
奥黛丽·赫本这个经典回眸，不知迷倒了多少男女。
至今这部电影还被奉为时尚宝典。
因为电影中赫本所有的幸福基本全由纪梵希亲自设计。
这个女人是美国时尚女性杂志主编，每期致力于引领美国女性的潮流风向。
可杂志现在却面临模特荒，因为这些模特虽然有一张美丽的外表，却缺乏更深层次的表现力。
于是，梅津与摄影师迪克带着团队浩浩荡荡来到了一家书店取景，他们擅闯的行为让店员桥很生气，他厉声制止，可这群人不为所动，不仅强行拉上他充当模特陪衬，将他锁在门外，还将书店糟蹋的一片狼藉。
梅津要选一个秀外慧中的女孩儿成为这本杂志的代表，可这些模特儿，都空有一副皮囊。
正当大家一筹莫展时，迪克提出让书店那个店员来担当女郎。
杂志虽然不太情愿，还是决定试一试。
于是他们通过订购书籍将桥请到了办公室，桥刚进入房间，一群人便粗鲁地对她评头论足，强行脱掉她的上衣，甚至还想上手剪掉她的头发。
桥很愤怒，她趁机逃离了这个房间。
结果为了躲避这群疯子的追赶，意外闯进了迪克的洗片房。
迪克晓之以理，动之以情，劝说桥答应他们的邀请。
一开始桥的态度很坚决，可当听到要前往巴黎时，她瞬间改变了主意。
巴黎有她最崇拜的哲学家胡安·霍斯曼教授，他是感情移入论之父，简单来说就是共鸣。
她一直期待着能够听到他的讲座，现在机会就在眼前。
就这样，巴黎之旅开始了。
可刚来到巴黎桥，就放了一堆人的鸽子，所有人等了她一天都不见踪影。
最后，迪克在一个咖啡馆找到了她，她正和一群法国人探讨共鸣的意义，可这群人根本听不懂英语。
不是做，而是基本上啊。
经过一番折腾，乔还是乖乖地来到了会场。
聚光灯落下帷幕，慢慢展开，乔像天使一般出现在众人面前，所有人都被她的美貌欢呼惊叹。
一周后的时装展上，她一定会大放异彩，可在时装展之前，他们还需先拍摄一组杂志。
这组杂志就算放在2021年，也依然是潮流风向标。
在火车的蒸汽下，她演绎了一个刚被丈夫丢弃的悲伤女人，在花圃中，她又化身陷入热恋的妙龄少女，坐在船上，她只是一个平民，为了吃饭在钓鱼。
好了。
多次拍摄的磨合，摄影师迪克已经与模特乔有了更深的默契，彼此都能理解对方的创作意图。
拍摄过程中，两人渐渐互生情愫。
终于在拍摄最后一组婚纱照时，乔率先表明了自己的爱意。
于是这片树林河小河就成为了他们爱情的见证。
很快，原定的时装展就要开始了。
乔正准备出门时，偶然得知他的偶像或异牟教授今晚会在咖啡馆演讲，于是乔顾不得展会，飞奔赶去见到她崇拜已久的异牟教授，也被他的相貌深深吸引，主动邀请她坐下，共同探讨哲学思想。
这时前来接乔去现场的迪克出现在了咖啡馆。
霍教授对乔做出的暧昧举动，让迪克醋意大发，不管叁七二十一，径自将乔拉走了。
看到乔一门心思的崇拜异牟教授，迪克气愤地警告他，霍教授根本不是以哲学家的身份接近学生，而是像男人接近女人一样接近她。
桥对迪克的说法感到很生气，认为迪克不仅侮辱了哲学，还侮辱了他。
两人在幕后争论霍教授是否对他有意思。
当帷幕拉开时，优秀女郎像落汤鸡一样蜷缩在角落，时装展成为笑柄。
为了挽回声誉，杂志主编决定重新举办时装展。
由于上次的经历，乔鸿雁担任模特，活动当天住所和咖啡厅都找不到他。
最终他们从酒店接待员那里得知模特招到霍教授的家里参加讲座去了。
乔的男友迪克和杂志主编赶到霍教授的住所，冒充一对歌手夫妇顺利混进去。
霍教授正在认真谈共鸣哲学，桥推开门正要将乔带回会场，但迪克与霍教授发生争执，不小心将霍教授打晕在地。
桥拒绝回到会场，大声斥责迪克让他滚出去。
迪克的态度伤害了桥，心情一气之下离开。
霍教授很快清醒，桥为他们的行为道歉。
但教授竟然对乔心怀不轨，乔才意识到。
迪克说的是对的，好在乔及时用瓷器打晕教授，禽兽才得以逃脱。
展会即将开始，只得一边走秀一边等待迪克的消息。
但为时已晚，迪克已经离开赶去机场了，最后是婚纱展。
桥看到那架飞往纽约的飞机，知道自己伤害了爱人的真心。
乔身着婚纱走在秀场上，满含热泪，成为了赫本最经典的一次回眸。
不等脱下婚纱就跑出了会场。
迪克在准备登机时偶然遇到了受会前邀请的人，知道了乔的所作所为，立刻赶回会场，但桥已经离开了。
二人就这样错过了吗？迪克仿佛想到了什么，他立刻驾车来到那片定情的树林。
果然，乔正一脸失落的呆在草坪上，终于，他们又像第一次拍摄。
婚纱是那样在草坪上翩翩起舞，两人幸福地拥抱在了一起。
其实这部电影剧情老套，但它无疑是一部时尚宝典。
影片中赫本的每一套服装都成为当时轰动时装界的单品，尤其是她蜕变之前的这身搭配，黑色紧身裤、黑色半高领毛衣、黑色豆豆鞋加白色袜子都成为大街小巷争相模仿的风向标。
除此之外，这部影片最有看点的还有舞蹈场面的设计，暗室里的双人舞、街灯下的独舞、迪克与煤矿工人在霍教授家里的合奏，还有那段让奥黛丽赫本大放光彩的咖啡师里的舞蹈，融合踢踏舞步和芭蕾的旋转，还有现代舞的灵动自由，让整部影片都绽放着赫本的个人风采。
另外，这部电影的男主是赫本最崇拜的一位舞蹈家。
所以不要再说男主老了，那可是我们女神的男神。
```

</div></div>
