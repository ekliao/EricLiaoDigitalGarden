---
{"dg-publish":true,"permalink":"/atomic-grouping-in-regex/","noteIcon":"2"}
---

date-created:: 2023-05-07

#Regex 
Closely related to possessive modifier, or is it the same?

## _Mastering regular expressions e3 (Jeffrey Friedl)_

Atomic grouping `(?> ̇ ̇ ̇)` will be very easy to explain once the important details of how the regex engine carries out its work is understood (p169). Here, I’ll just say that *once the parenthesized subexpression matches, what it matches is fixed (becomes atomic, unchangeable) for the rest of the match, unless it turns out that the whole set of atomic parentheses needs to be abandoned and subsequently revisited*. ==Still hard to understand== A simple example helps to illustrate this indivisible, “atomic” nature of text matched by these parentheses.

The string ‘¡Hola!’ is matched by !¡.+!," but is not matched if ! .+" is wrapped with atomic grouping, !¡(?>.+)!." In either case, ! .+" first internally matches as much as it can (‘¡Hola!’), but the inability of the subsequent !!" to match wants to force the ! .+" to give up some of what it had matched (the final ‘!’). That can’t happen in the second case because ! .+" is inside atomic grouping, which never “gives up” anything once the matching leaves them.

Although this example doesn’t hint at it, atomic grouping has important uses. In particular, it can help make matching more efficient (􏰍171), and can be used to finely control what can and can’t be matched (􏰍 269).

## _All about regular expressions (Jan Goyvaerts)_

An atomic group is a group that, when the regex engine exits from it, automatically throws away all backtracking positions remembered by any tokens inside the group. Atomic groups are non-capturing. The syntax is (?>group). Lookaround groups are also atomic.

(example)
...


