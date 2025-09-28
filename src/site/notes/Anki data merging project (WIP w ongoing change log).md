---
{"dg-publish":true,"permalink":"/anki-data-merging-project-wip-w-ongoing-change-log/","noteIcon":"2"}
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

tag: #(tag)
#（買）書a