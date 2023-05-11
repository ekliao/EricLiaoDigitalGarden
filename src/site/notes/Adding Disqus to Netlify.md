---
{"dg-publish":true,"permalink":"/adding-disqus-to-netlify/","noteIcon":"2","created":"","updated":""}
---

#mynote Perhaps it was partly serendipity and partly tenacity, I got Disqus working while having zero knowledge about componentization (include files, etc.) of a website. Credit all goes to [utsob](https://hermitage.utsob.me/ ) (my [thanks](https://glasp.co/highlight-embed?u=zeYBfVAGSvNl7zMHjBkmeoK0t0g1&d=GIk4F86kOFIl9B2B642P&h=9kwp7xbr8dfzjqlp&m=h) and the [context of the help](https://www.reddit.com/r/ObsidianMD/comments/10pokli/i_built_a_digital_garden_using_obsidian_for_free/)) for pointing the way twice. 

#project/aborted 
Steps
1. Register an account with [Disqus]([https://disqus.](https://disqus.com/)
2. Install it according to the site's [platform](https://ericliaointerpreting-netlify-app.disqus.com/admin/settings/install/). My site is built with [[Web publishing with Obsidian + Github + Netlify\|Github + Netlify]], not in the pre-defined list, so I had to [manually install Disqus using the Universal Code](https://ericliaointerpreting-netlify-app.disqus.com/admin/settings/universalcode/)
3. #paste/glasp/link I saw someone's [success](https://glasp.co/highlight-embed?u=zeYBfVAGSvNl7zMHjBkmeoK0t0g1&d=GIk4F86kOFIl9B2B642P&h=97ia3eqcu5xz4xij&m=h)

(The same highlight with #paste/glasp)
## r/ObsidianMD - I built a digital garden using Obsidian for free.

### Metadata

- Title: r/ObsidianMD - I built a digital garden using Obsidian for free.
- URL: https://www.reddit.com/r/ObsidianMD/comments/10pokli/i_built_a_digital_garden_using_obsidian_for_free/
### Page Comment

- #digital-garden #ob #Disqus #Netlify #commenting 

### Highlights & Notes

- Disqus is pretty easy. Just copy the universal code from Disqus. See the `note.njk` and `comment.njk` files in my repo: https://github.com/uroybd/topobon/
- I'm using Netlify's free tier
- It doesn't prevent you from adding Disqus. Just copy and paste the universal Disqus embed code from the Disqus dashboard, put it in a file in the `_includes` and import it in the note's template.

---
This majorly piqued my interest.
#project/aborted 
<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/10-dailynotes/2023-04-24/#7e438f" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



* Turns out, adding [Disqus](https://disqus.com/)-style commenting support to my digital garden wasn't as easy as it seems, by simply putting some universal code snippet (with one change) in a file under the `_include` directory. I hit a snag. 
	#paste/glasp/link  [My problem and getting further pointers](https://glasp.co/highlight-embed?u=zeYBfVAGSvNl7zMHjBkmeoK0t0g1&d=GIk4F86kOFIl9B2B642P&h=q7grki25c15lga58&m=h) 

</div></div>

Update: Success in the end.
#project/completed 

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/10-dailynotes/2023-04-26/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




## Hello, Disqus!

^7354c7

Hooray! I did it again! This time, I added [[Adding Disqus to Netlify\|Disqus]] commenting function to my website, following this failed attempt: 
<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/10-dailynotes/2023-04-24/#7e438f" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



* Turns out, adding [Disqus](https://disqus.com/)-style commenting support to my digital garden wasn't as easy as it seems, by simply putting some universal code snippet (with one change) in a file under the `_include` directory. I hit a snag. 
	#paste/glasp/link  [My problem and getting further pointers](https://glasp.co/highlight-embed?u=zeYBfVAGSvNl7zMHjBkmeoK0t0g1&d=GIk4F86kOFIl9B2B642P&h=q7grki25c15lga58&m=h) 

</div></div>
just a few days ago, all thanks to the kind owner of https://hermitage.utsob.me/ for pointing out what I did wrong.

The change is not perfect, for I discovered the wonky placement and disappearance of the light/dark theme switch on the page. Still, it's a rewarding feeling that putting in the work pays off.

### Pics or it doesn't exist

![Screen Shot 2023-04-26 at 01.09.24.png](/img/user/_attachments/Screen%20Shot%202023-04-26%20at%2001.09.24.png)

</div></div>

