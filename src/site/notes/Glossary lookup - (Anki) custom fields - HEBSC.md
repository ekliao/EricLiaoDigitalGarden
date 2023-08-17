---
{"dg-publish":true,"permalink":"/glossary-lookup-anki-custom-fields-hebsc/","noteIcon":"2","created":"","updated":""}
---

date-created: 2023-08-13

This documents my design of the "new" glossary management system, starting with Anki.
# Anki notetype

Inherit from Basic, not Markdown. The Markdown notetype requires installing an add-on to be able to render correctly. 
# Four essential fields: HEBS

## H = headword
This is the core word in an idiom or collocation. I get it that sometimes it's hard to choose one when two words seem equally important. Just settle for one. In that case, probably the word that comes first.
## E = entry
This is the full head entry. Can be a single word, an MWE (multiple word expression), or even a whole sentence.
## B = back
The meat of each Anki record. Contains part of speech (POS), definitions, examples, and sometimes a per-example source.
## S = source
The whole entry comes from this source. The source often the last identifying portion of a long hierarchical deck name, e.g. if the deck is `A::ROz::Bil::EC::JMYH`, the source is simply JMYH.
# Other Boolean fields in consideration (most essential first)

## C = collocation

By default, glossary entries are definitional and terminological, per popular belief. But I want to have an additional benefit: collecting collocations and their best translation and interpretation possible. 

This field by default will have no value (empty). But will have a single 'y' (yes) if the entry is DEFINITELY collocational, e.g. `unsolicited advice`.

What about PHRASES, SENTENCES, and IDIOMS?

Here's my thought for now:

IDIOMS are so fossilized that they should be treated as terms to be defined. So, don't turn on the C field for idioms.

PHRASES/SENTENCES should be considered to be the same. I won't collect a sentence unless there's a portion of the sentence that's collocational. The rest of the sentence can serve as context for that collocation.

In summary, any record is by default not collocational unless C:y. This has the elegance of needing only one Boolean field of C.

## I = idioms, P = phrases/sentences

I think based on the thinking above, these three fields are not necessary for now. Go for brevity and simplicity of design for now. Think of it this way: All my Anki entries used to have only two fields: front and back, or entry and back. Now, I've added H, S, and the single Boolean field C. It's already quite busy. I don't want to create any friction during data entry or indecision between whether something is phrasal or not.

# Recap

H
E
B
S
C (y)

These five fields will be my initial design. The card layout will follow this order:

E
B
S
H
C

Rationale: 

H comes last for textual entry. 

C is mostly empty or 'y' so logically should go last in data entry.

# First implementation

## 2023-08-17

![_attachments/Screen Shot 2023-08-17 at 16.02.43.png](/img/user/_attachments/Screen%20Shot%202023-08-17%20at%2016.02.43.png)

So glad I now have my most important deck (A-Dict) retyped as HEBSC. The search is more powerful with the addition of the 'h', 's', and 'c' fields. 
# Issues

I can see a struggle between the using the 'source' field and hashtags. Sometimes the source isn't clear. If I heard something on TV, from the radio, from watching a video, or simply by reading an article on the web or a post on some social media. Should it be of source=web or given a hashtag of web? 

For now, go for always filling out the source field (because it is defined) with one single piece of information, likely "web," if there's no better and more narrow description, like "netflix," "economist," (The Economist) or "nytimes" (The New York Times).
