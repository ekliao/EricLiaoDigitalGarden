---
{"dg-publish":true,"permalink":"/anki-data-merging-project-wip-w-ongoing-change-log/","noteIcon":"2","created":"","updated":""}
---

#rfp 
#project/started 
Take the normalized headword `inflection` as an example: produce the following single tab-separated value file

### Processing
- Rid of escaped double-quotes (") around or inside a field, so that one physical double quote is written as is without any escaping.
- Turn in-line \n characters into <br/>.
- Turn `#word` the content portion of a record into \_word\_ (surrounded by a pair of underscores)

# Output for New Anki Merged

## Headword (col 1)
`inflection\t`
## Record (col 2)
```
## Inflection n.<br/>
line 1
line 2<br/>
<br/>
{src:A::A-Dict}<br/>
{tags: #md #d/4}<br/>
<br/>
---<br/>
<br/>
## inflection, an<br/>
line 1<br/>
<br/>
{src:A::ROy::Bil::EC::JMYH}<br/>
{tags: #JMYH}<br/>
<br/>
---<br/>
<br/>
## inflection<br/>
line 1
line 2  
BrE _inflexion_ (line 3)
line 4<br/>
<br/>
{src:A::Aud}<br/>
{tags: #mw #aud #md}\t
```
## Tags (col 3)
``^merged mw d::4 aud JMYH md\n`

---
# Change log

20230630 retroactively:
```
The following action items need to happen early on in order to have cleaner data for the final normalizing and merging:

* in the headword field, look for

&apos;

and change into ‘ (ascii apostrophe),

look for 

&quot;

and change into “ (ascii double quote),

look for 

&#x27;

and change into ‘ (ascii apostrophe),

look for 

&lt;

and change into < (less than),

look for

&gt;

and change into > (greater than), 

look for 

&amp; 

and change into & (ampersand).

to recap, basically, restore 5 standard html named entities, plus one numeric hex entity for apostrophe into the original symbol, before further processing.
```

20230701 check status
```
Anki headword normalization

 • Remove beginning or training WS (whitespace)

 • Collapse multiple WS into one space character

 • Leave ##+ (two or more pound signs) intact

 • Replace a single # sign with a single space, then collapse resulting WS into one space character

 • Replace all full-width parens with their ASCII counterparts:

（ -> (
）-> )

 • Remove ending [{number}], and then the WS that trails:
Ford Motor [4] -> Ford Motor

 • Remove trailing articles:
<comma><space>(the|an|a)$

(Comma, followed by a space, followed by the, an, or a)

 • Remove beginning articles:

^(the|an|a)<space>

 • Remove trailing parts of speech (case sensitive):

<not-a-comma><space>(conj|pron|adj|adv|ad|vi|vt|v|j|n|d|r|a)\.?$
<not-a-comma><optional space>[\(\[\<](conj|pron|adj|adv|ad|vi|vt|v|j|n|d|r|a)[\)\]\>]\.?$

(trim away those trailing lowercase labels, surrounded by optional enclosing brackets, followed by optional dot; d = determiner or verb, j = adjective, r = adverb)

Don’t remove upper case labels such as N or ADJ.

 • Treatment of beginning or trailing words in parentheses:

Generally, remove any parenthetical expressions at the beginning or end of the headword, e.g.:

(Foo) bar -> bar
Foo (bar baz) -> foo

Exception:

Infix
 Foo (bar) baz -> Foo (bar) baz

Not separated by space
 (di)mid- -> (di)mid-

When it encloses Chinese characters (or anything that is not [a-zA-Z])

(一切)隨緣 -> (一切)隨緣

 • Lowercase everything [A-Z]->[a-z]
```

20230707 todo
```
each bullet or asterisk point is an action item:

* change all

<br>

into 

<br/>

* find regex

\s*<br/>\s*<br/>\s*<br/>\s*

(meaning: a series of at least 3 <br/> surrounded by optional whitespace)

replace with

<br/><br/>

(meaning: the end result is, there is at most one blank line between paragraphs and not more)

* in the end-matter of each record, for labels like {src: {tags: {line:, change the single colon (:) into a single equal sign (=), e.g.:

{src=A::A-Dict}

(reason: Anki can't search any single colon as literal and will return no hits)

* in the {src= portion only, change :: (double colons) into =- (an equal sign followed immediately by a hyphen), e.g.:

{src=A::A-Dict}

into

{src=A=-A-Dict}

(reason: while '==' is the more logical replacement for '::', the '==' has special meaning in Markdown (highlight, emphasis), but i just want the =- to be some unique separator for hierarchy of source)

* in the {tags= line only, don't print the 
{ #merged}


you still have it there, e.g.

{tags=^merged#JMYH}

should be:

{tags=#JMYH}

* also in the {tags= line only, add a space right after the tags=, e.g.:

change

{tags=#JMYH}

into

{tags= #JMYH}

(reason: Obsidian needs the space before the hashtag to recognize it as such)

* in the final, third tab-separated column, print 
{ #merged}


into the space separated list of tags. It's not there in the latest result.txt
```
