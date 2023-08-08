---
{"dg-publish":true,"permalink":"/tana-paste/","noteIcon":"2","created":"","updated":""}
---

date-created: 2023-08-07
#Tana 

Currently, I have high hopes of Tana Paste being the only way for me to import huge amount of glossary/terminology data into Tana.

[src](https://help.tana.inc/build-tutorials/tana-paste.html#:~:text=A%20Tana%20Paste%20is%20a,mjs%20myrepo%20%7C%20pbcopy%60.)

#paste/b 

![](https://firebasestorage.googleapis.com/v0/b/tagr-prod.appspot.com/o/notespace%2Fshaklev%40gmail.com%2Fuploads%2F2022-09-29T15%3A28%3A52.417Z-image.png?alt=media&token=8335be49-122a-48e4-a0f6-c26a8a2b04bf)

![_attachments/Screen Shot 2023-08-07 at 19.45.39.png](/img/user/_attachments/Screen%20Shot%202023-08-07%20at%2019.45.39.png)

Tana Paste is a way of generating rich Tana structures like fields, tags, dates, checkboxes etc, through a simple plain text paste. It is a bit slow, and not designed for inputting large amounts of information. In the future, Tana will offer proper plugin support. See video intro: [https://www.loom.com/share/6fd81ff1ab364acf9f448ffdedfeb57f](https://www.loom.com/share/6fd81ff1ab364acf9f448ffdedfeb57f).

A Tana Paste is a plain text paste that begins with the string '%%tana%%'. The easiest way to put this on the clipboard on a Mac is to cat a text file or run a command and pipe to pbcopy, for example `node github.mjs myrepo | pbcopy`. With your cursor on the block where you want the contents inserted, simply paste, and it will be transformed into Tana data structures and inserted. _Any output from external AIs or APIs are also automatically parsed by Tana Paste, and do not require '%%tana%%'._

The syntax is loosely modeled on Markdown. Nodes are prepended by '- ', and indentation indicates children.

Links use [[]]. This will look for a node in the Library of the current workspace matching that name. If none exists, a new node will be created and linked to. Multiple links with the same string will always point at the same node. You can also specify a node target using [[link name^uid\|]]. This will look for a node in the Library of the current workspace matching that name. If none exists, a new node will be created and linked to. Multiple links with the same string will always point at the same node. You can also specify a node target using [[link name^uid]]. If the uid does not exist, it will fall back to using the link name. If you only supply a uid, and it does not exist, it will create a link to "undefined", which you can later rename. (Note that we do not support more than one inline reference to a given node from a given node). If you also specify the tag of the link, like so: [[John Anderson #person\|John Anderson #person]], it will find a node named John Anderson and tagged #person anywhere in your graph, and link to that, or create a new node in the library with the provided tag.

Fields use :: between the field name and the value. Fields will look up by string, but if they are nested underneath a supertag which has any fields with that name, will prefer the field from the supertag definition. Like for links, you can specify a specific field using uid, like URL^uid:: value, which will also fall back to the string value, or an undefined field if no string name has been provided. If the field has a type of option or instance, and the provided value matches perfectly with an existing option or instance, the existing option or instance will be linked even if the text in the Tana paste is not a link.

![](https://firebasestorage.googleapis.com/v0/b/tagr-prod.appspot.com/o/notespace%2Fshaklev%40gmail.com%2Fuploads%2F2023-04-28T06%3A29%3A33.071Z-image.png?alt=media&token=eba9d2db-e270-44c5-b9b0-62ce9a6e3c88)

Tags use #, and multi-word tag names can optionally be wrapped in [[]], so either #bug or \|]], so either #bug or #[[my ideas]]. If no tag exists, a new one will be created. If you want to specify a specific tag, use ^ (#bug^uid). It will fall back to the string name, and if no string is provided and the uid doesn't match, the tag will not be created.

Fields with multiple values can be specified through a field name:: and then the values nested indented underneath

Images use the syntax ![](https://image.url)

Simple dates look like this: [[date:2021-02\|date:2021-02]]. They can also include time [[date:2021-02-01 20:30\|date:2021-02-01 20:30]], or only include the week [[date:2021-W02\|date:2021-W02]], month [[date:2021-02\|date:2021-02]] or year [[date:2021\|date:2021]], or even include a duration [[date:2021-02/2021-04-05\|date:2021-02/2021-04-05]]. We also still support the old format [[August 22nd, 2020\|August 22nd, 2020]].

Formatting: **bold** ^^highlighted^^ __italic__

Checkboxes use [ ] and [x] at the beginning of a node to indicate checked or unchecked. For fields/nodes which already have a checkbox, providing the [ ] will not change anything, but for other nodes/fields it will insert a checkbox. In all cases, [x] will correctly set the checkbox as checked.

You can find examples of scripts that output text in the Tana Paste format here [https://github.com/tanainc/tana-paste-examples](https://github.com/tanainc/tana-paste-examples)

Add  to a node to make it a search node (search expression indented under)

- In a search expression, we recognize system nodes (Set/Not set) and attributes (LINKS TO) etc.
    

You can also set the view of a node, using  , , or .

You can link to a tag using [[Tana Paste#tag\|#tag]] (especially useful in search nodes)

Tana Paste supports Markdown tables and code blocks.
#paste/e 
# Video tutorial
[video](https://www.loom.com/share/6fd81ff1ab364acf9f448ffdedfeb57f) by [[Stian\|Stian]]
- Video notes
	- `%%tana%%` begins Tana Paste section
	- To get help
		- [Tana Help Center](https://help.tana.inc/)
			- [Tana Paste](https://help.tana.inc/build-tutorials/tana-paste.html)
	- Github has Tana paste [examples](https://github.com/tanainc/tana-paste-examples)
	- **Some scripts**
		- Hypothesis: a tool to annotate web pages
			- Highlight, comment
			- Run script
				- Turn into tana paste ready format.
	- **Zotero**
		- Translator, quick copy
		- Direct paste into Tana!
	- ### Really interesting!
	- 