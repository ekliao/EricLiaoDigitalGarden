---
{"dg-publish":true,"permalink":"/tana/","noteIcon":"2"}
---

#PKM 
# Hello, Tana!

*(2023-08-07)* Just got early access to Tana. My first impressions: 
- Slick UI design
- Quick response
- In-context guide

Having played with Logseq, Tana's design philosophy is now very clear. I am on my way to try implementing my glossary/terminology management/lookup system.

Logseq's live query sucks. In comparison, from the way it looks, Tana's gonna rock in that department.
# At a glance

- Unified design: everything is a node
- AirTable + Notion + Roam
- An outlining app rather than writing app like Obsidian
- Supertags
- Cloud
- $10/month or $100 a year
- Still in beta, not a full publicly available commercial product
- Norwegian
# Pros

## Enforces structured/semantic data

## AI integration
- Get ready to have your mind blown: [Santi Younger's video](https://www.youtube.com/watch?v=6M8fPCBcwCY&list=PL_7j1BHf-xmirrPrmMi3LLzbfgEvk9oHS&index=11)
	- Not free
	- This seems way tighter integration than [[MEM.ai\|Mem.ai]]

# Cons
- Does not support long-form writing
	- [Long-form writing in Tana](https://ideas.tana.inc/posts/91-long-form-writing-in-tana)
		- A hack: [Santi Younger's video](https://www.youtube.com/watch?v=Gli6rFhjhXw)

- No web publishing of articles

Tana's web publishing works only through "workspace." Too much remains to be seen. I won't give up the current free and working Obsidian publishing solution for something this unknown.

#Glasp 
### Which Is The Best? Tana or Obsidian?

#### Metadata
- Title: Which Is The Best? Tana or Obsidian?
- Tags: #Tana, #Obsidian, #web-publishing
- URL: https://medium.com/talkingtech/which-is-the-best-tana-or-obsidian-4c15b1e1585d
#### Highlights & Notes
- Publish to web I’ve shared my digital garden online using Obsidian almost since the beginning. At first, I used Obsidian Publish and then started to experiment with different options, finally settling on the Digital Garden plugin.  I deleted my WordPress website and replaced it with my digital garden. It’s easy to update, even on my iPhone, a cinch to add new content and lends itself to writing.  Tana has an option to publish a workspace. I think this is to facilitate sharing templates at the moment rather than a full blown publication solution.

---
## Stian Horklev
#people 
### Video: Intro of Tana straight from the horse's mouth: Stian Horklev
[src: 回到Axton](https://www.youtube.com/watch?v=o-6b1UpxWYQ)
- Notes
	- Notion, AirTable
	- Backlinks
	- Outliner
	- Nodes (hierarchical)
	- Semantic structure through Supertags
		- Define something however you like
	- Tana templates (a bunch of fields)
		- Like creating applets or databases for anything
		- Sharable
	- Long ways to go to improve UI
	- AI
		- AI field
			e.g. AI-suggested action items based on YOUR content
			e.g. AI giving you critique of a plan
		- System of commands ("Tana Commands")
	- Command nodes
		- Ask AI
		- API
			- Webhooks
				- Whatsapp
				- Telegram
			- Automation / handshakes with other apps
	- Ecosystem (long-term goal)
		- Integration
		- Plugins
		- API
	- Input API
		- e.g. let GPT do some magic/coding for you, given sample data, like airline itineraries
		- AI for app builders
			- LangChain
	- Onboarding is a challenge for new users not familiar with workflows
	- Likely freemium model
	- AI is expensive

### Tana Paste

Markdown-like input text into Tana structures.

- [Video by Stian](https://www.loom.com/share/6fd81ff1ab364acf9f448ffdedfeb57f)

---
## Ev Chapman 
#people 
### [Video: Ev's first week with Tana](https://www.youtube.com/watch?v=3Jhr_xDPKvI&t=305s)
- #videoNote 
	- Block-based Outliner like Roam + database/structured data like Notion
	- Demo node: "idea for a long-form article"
		- Supertag
		- "Opening" a node = expand the bullet point
			- Reveals some fields like "status," "type." Are they built-in or user-defined?
		- Add a tag ("#spark idea")
			- Configure the tag (e.g. "#spark idea")
			- Here, "status" and "type" are shown as the first two fields, suggesting they are user-defined.
			- Define "default content"
				- e.g. "Brain dump" : a child node!
			- Define each field
				- type
		- Add another tag (e.g. "#YouTube video")
			- It gets its own default content: "YouTube script" node
				- Can have children nodes, further defining the "YouTube script" parent node
			- The fields of this tag can have the same name, e.g. "type"
				- Can identify/pick the same "type" field as used in "#spark idea"
	- Live searches
		- Construct a query (with auto-complete help), which can be named
			- Generates a list of nodes
			- Different views (e.g. table)
			- Can be filtered (through field values)
			- Her "Content Hub," mentioned by Note Aloud (Nicola Fisher) as inspiring, is an example of a named live search.
	- Foreshadows future introduction of Tana "workflows"

![[_attachments/Screen Shot 2023-07-12 at 01.59.54.png\|600]]

In 8 minutes' short video, E did a wonderful job getting me sold on Tana's main feature: Notion-like semantic structure.

---
## CortexFutura
#people 
### [Video: Tana fundamentals 01: UI](https://www.youtube.com/watch?v=WqASI-p-dJM&t=57s)
- #videoNote 
	- A node's bullet point with gray outer circle means it's collapsed.
		- Exactly like Logseq (or Workflowy)
	- Quick keyboard shortcuts to go up or down the indentation tree of nodes
	- Root node
		- Automatically contains
			- Calendar
			- Todo
			- Everything else (nodes)
	- Command prompt: CMD+K
		- Can sort nodes
	- TanaLab
		- Regex search
	- CMD+E for quick add to daily node

### [Video: Tana fundamentals 02: Everything is a node](https://www.youtube.com/watch?v=v6C7t6l8iL4)
- #videoNote 
	- Two ways of referencing:
		- At the beginning of a node, use @ sign to create "backlink" or "reference node"; it is identified by dotted line outline of the bullet point.
		- It works like embedding in Obsidian
			- But can be edited directly.
		- Inline reference: use also the @ sign. Shows as a link (underline). Click on it to visit the node.
			- If the referenced node hasn't been created, you'll be prompted to create it, and it goes under the Library node (child of root).
			- SHIFT-click will embed it below the node.
	- MOVE TO command, 3 destinations
			- Home
			- Library
			- Today
	- Backlinks are shown at the end of a node, the "referenced in" section.
	- Views
		- as table
		- as list
		- as cards
		- as columns
		- as tabs
	- 
### [Video: Tana fundamentals 03: Data about nodes](https://www.youtube.com/watch?v=f4FcNhlU7G4)
- #videoNote 
	- Think of a tag as a relationship.
		- e.g. "Washington: A Life" is a book. Give it a tag named "book". Here, the relationship is: "is a book."
	- Indent under a node with a tag (tab), then type ">" (greater than) to create a field under the tag.
		- e.g. "Author"
			- Any previously created field names will be shown as prompt (auto-complete) when creating a field in the future.
			- Notice how a tag can be created for the value of this "Author" field (the value is the name of the author).
				- This Author tag seems to serve a different function than the Author field.
					- Duh! The Author tag is a supertag, a template. The Author field is very insignificant.
						- Appreciate the subtlety!
	- CMD-K: configure a field
		- name
		- description
		- field type
			- Anything (freeform data)
			- **Instance of an existing tag** (shown as `#instance`)
				- This is great convenience. Will remind you to add a tag in the future for the same field name.
	- Can use mouse to select multiple consecutive nodes and apply bulk change
		- e.g. add a tag
	- Tags can contain spaces
		- e.g. "US President"
	- Can tag a linked new node. 
		- @ to create the link
		- Use arrow key to select the link (shows a thin blue outline)
			- ![[_attachments/Screen Shot 2023-08-07 at 23.55.54.png\|200]]
		- CMD-K to add a tag to it.
			- The tag won't show on current page, but it is added to the linked node:
				- ![[_attachments/Screen Shot 2023-08-07 at 23.57.16.png\|100]]
				- #progress  
				- 
- OLDER video notes
	- CTRL-I to add a description to any node
	- Fields
		- Field types
		- Default tags
	- Tags
	- \@ to reference a node
		- Typed backlinks: powerful concept
	- Views
		- Table view
			- Add a new field to the view
				- e.g. "Topic"
					- Value "US Presidents" itself is also a node

### [Video: Tana fundamentals 04: Live Search](https://www.youtube.com/watch?v=ohisZOdNNFY)
- #videoNote 
	- #todo/watch
	- 

---
## Santi Younger
#people 
[Video: Interviewing Riccardo Busetti](https://www.youtube.com/watch?v=wj2jvd7wmjs&list=PL_7j1BHf-xmirrPrmMi3LLzbfgEvk9oHS&index=4)
- Notes
	- Cloud/sync
		- Not necessarily bad if secure
		- Pro: accessible everywhere with Internet
	- Tana has made Notion/Roam/Logseq obsolete
	- Can Tana replace Obsidian?
		- Yes if it decides to expand the node for long-form writing
	- Lacking Heptabase visuals
		- Can be built too
	- SRS: go with Anki or Mochi
	- Craft for long-form writing
		- Sharable
		- Aesthetic
	- Notion is strong with sharing/creating website
		- Santi did this but moved to [[Webflow\|Webflow]], more powerful, more options

### Fred Jame
#people 
#paste/b 
[src](https://www.facebook.com/thefredjame/posts/pfbid0xhrPZxFEoBJAGBWsU7pMCGogcLESZb972WhUbwUBipxgSj4tVJmc9SpttfXDd6czl?__cft__[0]=AZVx0Kh3ikZfbNuIimJ3EG3hQeU5A26wrOyJtpgC42-KeH_g1DdS_tLc7AVdaKTZ8F7g6ecxVc2oAJDzqk8O55t082DjjQHwXd2Kl8aSrpcTna5MSr7_TP7bzACFtIjpFX4eSQymQnafis6PtTSS0IRh6O1RcMQ85GmBbqxCbVlOVzFs1ZYdGqiCVOI0_IesdeU&__tn__=%2CO%2CP-R)  

這兩天花最多時間做的事是深入玩Tana和AI功能的整合。雖然還不是很完整，但Tana的資料使用彈性和AI整合深度大概贏Notion有5個馬身。

但如果這些功能用不到，只是單純的做筆記，兩者的差異就沒那麼大，甚至Notion還簡單一點（會說Notion「簡單一點」，就知道Tana有多強）。

但Tana的弱點在於：

1. 資料的展現方式（字體變化、排版等等）遠不如Notion

2. 缺乏與外部資料（行事曆、通訊錄、其他SaaS等）的連結整合

3. 資料很難變成共通格式（PDF之類）跟其他軟體共享、或用於列印

4. 用於收集資料（錄音、照相、辨識文字）的手機版Tana Capture工具很好用，錄到的聲音可以在網頁版上轉成正確度相當高的文字檔（中文也可以），但目前還沒有行動app，只能用在行動裝置上很難用的網頁版。