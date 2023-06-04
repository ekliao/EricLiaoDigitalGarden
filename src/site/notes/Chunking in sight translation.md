---
{"dg-publish":true,"permalink":"/chunking-in-sight-translation/","noteIcon":"2","created":"","updated":""}
---

#workInProgress 
This is a note I quickly whipped together after attending the first couple of weeks of a refresher course on sight translation (henceforth ST). It reflects my thinking out loud about developing mechanical steps in identifying a chunk in ST.

# What constitutes a Chunk?

It has much less to do with grammatical and syntactical phrasal constituents and more to do with:
- speech
	- natural pauses
	- connected speech
- meaning
	- meaning units
	- logical flow
- conversion strategy
	- SL word order
	- insertion of “connectors” (not the same as grammatical conjunctions)

# A Crucial Question

Should there be out-of-order translation within a chunk? 

Pondering this, first we observe that we want this to be true:

A: A chunk to be as long as possible.

Reducing the number of chunks naturally means less pre-processing before rendition.

B: If chunk X precedes chunk Y, we naturally want to render X first without considering the content of Y.

That is, we think of the slash (or double slashes) to serve as a mental stop, a barrier between two chunks, and hence we intuitively want this.

C: Within a chunk, we intuitive want to render in the same SL order.

This idea is also self-explanatory.

Now, the problem is, we cannot have all of A + B + C. If that were the case, it's not possible to render into TL without reversing SL word order. Since we know it is impossible for any TL to have exactly the same word order as SL (at least, that's absolutely the case between English and Mandarin Chinese), we can't enjoy all three conditions.

The question is, which condition should we let go to still enjoy maximal efficiency in sight translation (henceforth ST)?

At first blush, we realize that B and C are diametrically opposed. They are absolute conditions while A is a matter of degree, a nice-to-have.

In my opinion, having thought about the three conditions, I definitely will choose to sacrifice C first. 

Let's game it out:

Scenario 1: Giving up C actually contributes to enhancing A (1 point). Insisting on C actually hurt A a lot (0.25~0.5 point, to be used below) and makes B impossible (0 point), so we get 2 points.

Scenario 2: Giving up B (preserving C) results in lots of chunks especially single functional word chunks. This practically destroys A as mentioned above (0.25 point). So we get 1.25 points, or 1.5 points at best.

Scenario 3: Insisting on A does not make sense. In the extreme, the entire passage is one chunk. This will definitely violate B and C. Where do we draw the line? If we try to slice up the passage into just two chunks always, there's still no guarantee to meet both B and C. So we go shorter and shorter. But which of B and C do we always strive to meet? We can't be wishy-washy, sometimes going with B and sometimes C. Doing so would render the chunking process meaningless. So, scenario 3 is not valid.

The verdict, then, is that we always satisfy B while meeting A as much as we can. Restating as rules:

1. If adjectival, adverbial, or subordinate clauses are detected, they must be NO chunking before those elements. The chunk is lengthened until the end of those elements where it is safe to chunk.
2. After the chunking is made (by a slash or double slashes), quickly underline or circle the beginning word of the said element, and draw an arrow pointing toward earlier text, at the place where the element should be rendered.
3. Naturally, if there is no chunk separator at at point, add one there too, to enforce condition B.
4. Where there are no such elements, make the chunk as long as you can.
5. This means that at the beginning of a chunk, most attention is to be devoted to rendering the subordinate elements first.
6. This approach makes the chunk separator serve double duties as a visual cue of danger. It gets the most bang for the buck spent on chunking. This makes great sense.

#todo We should think about the opposite approach of preserving C while abandoning B to actually evaluate whether it may makes more sense at least sometimes.

Continuing on this settled approach: so far we assume we'll do more literal rendition preserving parts of speech and syntax of SL into TL. This will often result in very awkward rendition especially from English into Mandarin Chinese, such as a super long ...的 pre-nominal phrase. We need to add the strategy of going with the SL phrasal order as much as possible, chunking at problem spots while adding appropriate “connectors” between two chunks to smooth the flow of meaning and speech.

Happily, this strategy is shared by simultaneous translation, where following SL phrasal order is key to success. It's called the salami technique, or _[saucissonnage](https://en.wiktionary.org/wiki/saucissonnage)_ in French if we want to be fancy.

---
## More...

[[Syntactic linearity 順句驅動\|Syntactic linearity 順句驅動]]