---
{"dg-publish":true,"permalink":"/perl-6-notes/","noteIcon":"2","created":"","updated":""}
---

# Books

I am learning Perl 6 mainly with these two books.

## [[book - Parsing With Perl 6 Regexes and Grammars, 2017, Moritz Lenz, Apress\|Parsing With Perl 6 Regexes and Grammars, 2017, Moritz Lenz, Apress]]

## [[book - Learning Perl 6, 2018, brian d foy, O'Reilly\|Learning Perl 6, 2018, brian d foy, O'Reilly]]

# Insights

## Whitespace (ws)

- `token` and `rule` are different from `regex` by adding ratcheting (non-backtracking).
- `rule` also inserts `<.ws>` **ONLY** where there is a literal space, specifically:
	- After terms and other named things
	- ***But not*** at the beginning of the rule #todo/verify

### An over-the-top but super clarifying example

To absolutely understand ws handling, here's some actual code (fn1) to confirm what I suspect to be true.

```
my token tn {<alnum>}  
my token t {\d \d}  
my token t_anchored {^ \d \d $}  
my token t_trailing_backslash_s {\d \d\s}  
my rule r {\d  \d}                        # two spaces  
my rule r_nospace {\d\d}  
my rule r_nospace_from_named {<tn><tn>}  
my rule r_space_from_named {<tn> <tn>}  
my rule r_training_space {\d  \d }        # two spaces 
my rule r_training_backslash_s {\d  \d\s} # two spaces 
```
Output:

Each of these 16 cases has been confirmed.
```
「42」 matched token t {\d \d}
「 42」 matched token t {\d \d}
「 42」 does not match token t_anchored {^ \d \d $}
「4 2」 does not match token t {\d \d}
「42」 does not match token t_trailing_backslash_s {\d \d\s}
「42」 does not match rule r {\d  \d}
「42」 matched rule r_nospace {\d\d}
「4 2」 does not match rule r_nospace {\d\d}
「4 2」 does not match rule r_nospace_from_named {<tn><tn>}
「42」 does not match rule r_space_from_named {<tn> <tn>}
「4 2」 matched rule r {\d  \d}
「4  2」 matched rule r {\d  \d}
「4   2」 matched rule r {\d  \d}
「 4   2」 matched rule r {\d  \d}
「 4 2」 matched rule r_training_space {\d  \d }
「 4 2」 does not match rule r_training_backslash_s {\d  \d\s}
```

---
fn1: I had to use the `.gist` method and the `&` method reference in `&t.gist` to print `token t {\d \d}`. I hope I'll learn an easier way to stringify a regex object.