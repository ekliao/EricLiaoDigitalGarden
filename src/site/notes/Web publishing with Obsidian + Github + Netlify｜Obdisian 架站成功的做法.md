---
{"dg-publish":true,"permalink":"/web-publishing-with-obsidian-github-netlify-obdisian/","noteIcon":"2","dg-note-properties":{"date-created":"2023-04-15","creation_date":"20230415"}}
---

(Update)

*20231023* - The original web page of Feng's blogpost referred to below is gone, as he announced the loss of the content this month in a short [post](https://www.fengrin.me/blog/my-first-post) (update 20240714 - even this announcement itself is now gone.) Luckily, I copied and pasted the original text below. Unfortunately the images are broken and lost. The moral: Back up your good stuff. 好東西記得備份！

---

This is the main guide, with thanks to [Feng Zhang (峰的博客)](https://fengrin.me/), that directly helped me build the website you're seeing. Its opening paragraphs enticed me with the idea of "publishing at the push of a button" (通過命令一鍵發布). It provides high-level steps without going into detailed steps, but luckily I managed to figure them out, especially the seemingly magical yet baffling parts of Netlify's role in this undertaking.

(Update) 

*20230727* - For detailed guide straight from the horse's mouth, see "Related Resources" at the bottom of this page.

*20240714* - Note that images from Feng's post are not viewable in its original source (link below).

#project/learn-by-doing 
#paste/b 
[src: Feng's blog post](https://fengrin.me/posts/2022-12-19-publish-your-website-free-use-your-local-note-obsidian-gitHub-netlify)

---
## 免費直接把筆記發布成網站: Obsidian+GitHub+Netlify

December 19, 2022

Hello，大家好，今天向大家介绍，如何免费用 Obsidian + GitHub + Netlify 发布自己的网站。简单的说，Obsidian 是一个 markdown 笔记软件，GitHub 是一个代码托管网站，Netlify 是一个静态网站部署工具。

建好之后，流程大致是，在 Obsidian 编辑文章，然后==通过命令一键发布==【巜 This sounds too good to be true】，然后就可以通过网址访问了，这里有其他人建好的，大致是这个样子：

-   1: [EDAV Garden](https://edav-garden.netlify.app/)
![image](https://cdn.fengrin.me/2022/2022-12-19-publish-your-website-free-use-your-local-note-obsidian-gitHub-netlify-2.png)

-   2: [Razvan Andrei Surdu](https://razvan-andrei-surdu.eu/)
![image](https://cdn.fengrin.me/2022/2022-12-19-publish-your-website-free-use-your-local-note-obsidian-gitHub-netlify-3.png)

0 准备：

-   下载 Obsidian 笔记软件
-   注册 [[GitHub\|GitHub]] 账号

1 首先，我们需要用到 Obsidian 的一个插件 [Digital Garden](https://github.com/oleeskild/obsidian-digital-garden)，下载安装Digital Garden。

2 打开这个 [repo](https://github.com/oleeskild/digitalgarden)，点击绿色的 deploy to netlify
> I don't see any green button for that. But I managed to "create depo". #todo Document details.

这样会打开 Netlify，在你的 GitHub 创建一个这个 repo 的 copy。然后新建一个名字，然后按步骤在 Netlify 发布你的网站到 internet。

3 下一步，你需要获取你 [[GitHub\|GitHub]] 账户的 access token，这个 token 用于你的 Obsidian 笔记软件的设置，相当于一个 password。去[这个网址](https://github.com/settings/tokens/new?scopes=repo)，点击 generate token 按钮，复制 token，下一步需要用到。

4 打开 Obsidian - Digital Garden 的 settings。填入 [[GitHub\|GitHub]] 用户名，repo 的名字（在 step3 设置好的），还有上一步复制好的 token。

5 现在可以发布你的第一个笔记了。在 Obsidian 创建一个新的笔记，并且把下面字符加到笔记的开头。

```
---
dg-publish: true
dg-home: true
---
```

笔记现在它应该是这样的：![image](https://cdn.fengrin.me/2022/2022-12-19-publish-your-website-free-use-your-local-note-obsidian-gitHub-netlify-1.png)

-   dg-home 代表这个笔记应该作为网站首页
-   dg-publish 设置代表这个笔记是否需要被发布到互联网上。

6 按 CTRL+P 打开命令面板，找到 Digital Garden: Publish Single Note 命令，按回车。

或者，点击侧边栏的小树苗 🌱 的图标，然后点击发布按钮：
![image](https://cdn.fengrin.me/2022/2022-12-19-publish-your-website-free-use-your-local-note-obsidian-gitHub-netlify-4.png)

7 在 Netlify 找到你网站的网址，打开，大功告成：
> No step-by-step guide about how to do this finding! But again I managed to find my way and it all worked. #todo Add details.

![image](https://cdn.fengrin.me/2022/2022-12-19-publish-your-website-free-use-your-local-note-obsidian-gitHub-netlify-5.png)

### 如何添加 Connnected Pages 图表

0 例子：

![example](https://cdn.fengrin.me/2022/2022-12-19-publish-your-website-free-use-your-local-note-obsidian-gitHub-netlify-6.png)

1 点击 Obsidian - settings：

![obsidian - settings](https://cdn.fengrin.me/2022/2022-12-19-publish-your-website-free-use-your-local-note-obsidian-gitHub-netlify-7.png)

2 点击 settings - Appearance - Manage：

![obsidian - settings](https://cdn.fengrin.me/2022/2022-12-19-publish-your-website-free-use-your-local-note-obsidian-gitHub-netlify-8.png)

3 ==选择支持图表的 Theme，如 Wikipedia==
> Great. So, it's possible to choose a theme. The results of a nice theme like `Red Graphite`, with its san serif fonts, are much more beautiful and modern-looking than the default's serif fonts.

![obsidian - settings](https://cdn.fengrin.me/2022/2022-12-19-publish-your-website-free-use-your-local-note-obsidian-gitHub-netlify-9.png)

4 点击 settings - Note Settings - Edit

5 开启：Show local graph for notes:

![obsidian - settings](https://cdn.fengrin.me/2022/2022-12-19-publish-your-website-free-use-your-local-note-obsidian-gitHub-netlify-10.png)

6 添加 [Internal link](https://help.obsidian.md/How+to/Internal+link)

创建一个 Note，名为 hi i am Refo Zhang

创建一个 Note，名为 digital garden

在 Obsidian 中，编辑 digital garden note，按键盘上的 `[` 两次，然后输入 hi，选择弹出的 hi i am Refo Zhang。最终效果是：

```
[[hi i am Refo Zhang]]
```

这样就会在第二个 note 中，创建一个第一个 note 的 internal link。

7 Publish 所有的改变，即可得到一个含有所有 Notes 关系的图表

#project/completed 
#paste/e

---
## Related resources

- Another [short article in Chinese](https://anotherdayu.com/2022/4222/) that supposedly describes the same process. #todo/verify 
	- This is a brief translation of the very detailed official English [guide](https://dg-docs.ole.dev/getting-started/01-getting-started/) by the author of the Digital Garden plugin, hosted on a site enabled by the plugin itself. How apropos!
	- The guide itself spans several steps and pages.
- [How to Set Up a Digital Garden With Obsidian For Free](https://www.youtube.com/watch?v=kg-9n_A4Tf0) #todo/verify Watch to see if it's a better step-by-step guide and alternative to Feng's article (this one).
- A new but different [video](https://www.bilibili.com/video/BV1HF411173m/?spm_id_from=333.337.search-card.all.click&vd_source=c5814fc82506100ec4b07566dc20d79f) guide of the same setup. I haven't gone through it, but it looks straightforward.
# Issues

- [[Obsidian Digital Garden Plugin + Netlify build failure scares｜Obsidian 網站建置失敗\|Obsidian Digital Garden Plugin + Netlify build failure scares｜Obsidian 網站建置失敗]]