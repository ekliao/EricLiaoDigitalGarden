---
{"dg-publish":true,"permalink":"/regex-conditionals/","noteIcon":"2"}
---

#Regex  
*(2023-05-06)* Since I caught the regex bug yesterday (I hadn't been in a long time), I set out to learn the always elusive negative lookbehind. 

Update: turns out what ended up working was a negative lookahead (see below). I obviously still haven't grasped the concept well.
## Task description

I wanted to detect and fix files (in markdown) that contains any `<(紅|黑|不|...)>`, i.e. the popular GRE vocab data from the web, but without the `#d/Mydict/vocab/RedGemEtc` tag preceding it. I want to insert the missing tag right after `#d/Mydict` to make it complete.

E.g. this should be bypassed:

```
---
anki-front:_attorney_
anki-deck:A::A-Mydict
---
#d/Mydict
#d/Mydict/vocab/RedGemEtc

(...)
<紅>律師
```

while this should be detected:

```
---
anki-front:_attorney_
anki-deck:A::A-Mydict
---
#d/Mydict

(...)
<紅>律師
```

While failing again to craft a regex that worked for the problem above, I managed to use a trick (using `#d/Mydict\n[^#]` as anchor) to solve the same problem. But I was ever more frustrated that still didn't have proper knowledge regarding lookbehind (henceforth LB).

I dawned on me that I had read about regex conditionals in the admirable tutorial site by Jan G. So I went there again to learn of the syntax. I also visited rexegg, the also amazing sister site. I soon noticed the two authoritative sources seem to show different syntaxes for regex conditionals. Why? I'm so confused.

https://www.regular-expressions.info/conditional.html
https://www.rexegg.com/regex-conditionals.html

I set out to try both syntaxes on [regex101](https://regex101.com). No joy. Complete frustration!

Then I found this [YouTube](https://www.youtube.com/watch?v=tblSuwP6sAY). More confusion.

#paste/b 
Q:
![Screen Shot 2023-05-06 at 08.11.44.png](/img/user/_attachments/_OB/Screen%20Shot%202023-05-06%20at%2008.11.44.png)

A: 
![Screen Shot 2023-05-06 at 08.12.51.png](/img/user/_attachments/_OB/Screen%20Shot%202023-05-06%20at%2008.12.51.png)

![Screen Shot 2023-05-06 at 08.13.29.png](/img/user/_attachments/_OB/Screen%20Shot%202023-05-06%20at%2008.13.29.png)
#mynote I tried the suggested `^(A)?(?(1)X|G)` in regex101 and [[CotEditor\|CotEditor]]. Neither worked.
#paste/e 

---
## Perl community

Next, I invoked the Perl genie:

[src](https://stackoverflow.com/questions/14091965/conditional-regular-expression-with-perl#:~:text=Yes%2C%20Perl%20supports%20conditional%20expressions,any%20characters%20in%20the%20string.)
#paste/b 
Q: Does Perl support conditional regular expression :

```perl
(?(condition)true-pattern|false-pattern)
```

i.e. if the condition is true then try to match the true pattern else try to match the false pattern

If Perl supported conditional regular expressions then why didn't this code print `1`?

```perl
use strict;
use warnings;

$_ = 'AB';

if ( /(?(A)B|C)/ ) {
  print 1;
}
```

A1: Your regex doesn't just not match, it throws the following syntax error:

```perl
Unknown switch condition (?(A) in regex; marked by <-- HERE in m/(?( <-- HERE A)B|C)/
```

That's because `A` is not a valid condition.
#mynote Huh!

A2: I know I'm late this question but I'll try to explain my understanding of what the current regex is doing and how it can be adjusted.

Yes, Perl supports conditional expressions. However, the problem with this regular expression is that ==the condition has to either be a back reference or a zero-width assertion like a look-behind or look-ahead. In other words, the conditional can never consume any characters in the string.==
#mynote Ah! 💡

So let's look at a couple ways that this can be rewritten.

One way would be to use a look-ahead and add the match to the `then` expression. So it could be rewritten to `/(?(?=A)AB|C)/`. This says if the string matches `A` then match and consume `AB` else match and consume `C`. This would then successfully match either `AB` or `C`.

Another way would be to use a capture group before the condition like so `/(A)?(?(1)B|C)/`. This says match and consume `A` zero or one time; if capture group `1` has a match then match and consume `B` else match and consume `C`. This would also successfully match either `AB` or `C` same as the previous example because the `A` is consumed and moves the match forward if it is present in the string.

[The perldoc](http://perldoc.perl.org/perlre.html#Extended-Patterns), as referenced in the other answer, explains other options you can use in the conditional but I feel the two examples above would be the most common to use.

#paste/e 

Soon I began suspecting that neither regex101 nor CotEditor supports regex conditionals. So I turned to [[EmEditor\|EmEditor]]. I Googled about Onigmo and soon found guide at the bottom of this page.

---
## EmEditor Onigmo.regex 

Onigmo is the C++ regex engine that supports things like `\p{Han}`. Now, its support for regex conditionals is confirmed:

## tl;dr
{ #32a3c2}


The example toward the end in the guide that uses a lookahead regex containing `.*(thing)`, making it variable length, supported my suspicion about the cause of failure, gave me hope, and sparked some creativity. I soon tinkered around more in regex101 for a good half hour, and eventually as I was about to give up...

🥁 🧻 please... Bingo! I crafted a successful match in regex101, which was then confirmed in EmEditor, in blue highlight:

(Also, I hereby confirm that unfortunately [[CotEditor\|CotEditor]] does not support regex conditionals.) 
{ #75709c}


![Screen Shot 2023-05-06 at 09.13.46.png|550](/img/user/_attachments/_OB/Screen%20Shot%202023-05-06%20at%2009.13.46.png)
{ #84deef}


![Screen Shot 2023-05-06 at 09.14.01.png|500](/img/user/_attachments/_OB/Screen%20Shot%202023-05-06%20at%2009.14.01.png)

I want to etch this magical example into my brain lest I forget it:

# `^(?!(.*RedGemEtc)).*(?(1)xyzzy|<.>)`

This alternative also worked:

# `^(?!.*(RedGemEtc)).*(?(1)xyzzy|<.>)`

The regexes match

`a baz blahblah foobar <紅> a`

and reject

`b baz RedGemEtc foobar <黑> b`

as expected.

## Key points
*(most important first)*

- The `.*` after the lookahead is key. Without it it will never work. Because regex is about thinking constantly about the current position in the subject string vs the pattern: does it match or not; does it consume characters or not, etc.
	- This `.*` should be outside (after) the lookahead parens. I don't know why.
- There should be another `.*` inside and at the beginning of the lookahead pattern.
	- It should not be outside and before the lookahead.
	- However, it can be inside or outside the capturing group, depending on your need.
- Use the `^` or `\A` anchor.

## Try this regex yourself

Come [here](https://regex101.com/r/FtCE2u/1) to give it a try on regex101. Cool, eh?

---
## The guide that helped
[src](https://www.honeybadger.io/blog/using-conditionals-inside-ruby-regular-expressions/#:~:text=As%20it%20turns%20out%2C%20the,inside%20of%20your%20regular%20expressions.)
#paste/b 

As it turns out, the Onigmo regex engine has a few neat tricks up its sleeve including the ability to use conditionals inside of your regular expressions.

...

### Conditionals

Conditionals in regular expressions take the form `/(?(A)X|Y)/`. Here are a few valid ways to use them:

```
# If A is true, then evaluate the expression X, else evaluate Y
/(?(A)X|Y)/

# If A is true, then X
/(?(A)X)/

# If A is false, then Y
/(?(A)|Y)/

```

Two of the most common options for your condition, `A` are:

-   Has a named or numbered group been captured?
-   Does a look-around evaluate to true?

Let's look at how to use them:

#### Has a group been captured?

To check for the presence of a group, use the `?(n)` syntax, where n is an integer, or a group name surrounded by `<>` or `''`.

```
# Has group number 1 been captured?
/(?(1)foo|bar)/

# Has a group named "mygroup" been captured?
/(?(<mygroup>)foo|bar)/
```

##### Example

Imagine you're parsing US telephone numbers. These numbers have a three-digit area code that is optional unless the number starts with one.

```
1-800-555-1212 # Valid
800-555-1212 # Valid
555-1212 # Valid

1-555-1212 # INVALID!!
```

We can use a conditional to make the area code a requirement only if the number starts with 1.

```
# This regular expression looks complex, but it's made of simple pieces
# `^(1-)?` Does the string start with "1-"? If so, capture it as group 1
# `(?(1)` Was anything captured in group one?
# `\d{3}-` if so, do a required match of three digits and a dash (the area code)
# `|(\d{3}-)?` if not, do an optional match of three digits and a dash (area code)
# `\d{3}-\d{4}` match the rest of the phone number, which is always required.

re = /^(1-)?(?(1)\d{3}-|(\d{3}-)?)\d{3}-\d{4}/

"1-800-555-1212".match(re)
#=> #<MatchData "1-800-555-1212" 1:"1-" 2:nil>

"800-555-1212".match(re)
#=> #<MatchData "800-555-1212" 1:nil 2:"800-">

"555-1212".match(re)
#=> #<MatchData "555-1212" 1:nil 2:nil>

"1-555-1212".match(re)
=> nil

```

##### Limitations

One problem with using group-based conditionals is that matching a group "consumes" those characters in the string. Those characters can't be used by the conditional, then.

For example, the following code tries and fails to match 100 if the text "USD" is present:

```
"100USD".match(/(USD)(?(1)\d+)/) # nil
```

In Perl and some other languages, you can add a look-ahead statement to your conditional. This lets you trigger the conditional based on text anywhere in the string. But Ruby doesn't have this, so we have to get a little creative.

### Look-around

Fortunately, we can work around the limitations in Ruby's regex conditionals by abusing look-around expressions.

#### What is a look-around?

Normally, the regular expression parser steps through your string from the beginning to the end looking for matches. It's like moving the cursor from left to right in a word processor.

Look-ahead and look-behind expressions work a little differently. They let you inspect the string without consuming any characters. When they're done, the cursor is left in the exact same spot it was at the beginning.

For a great introduction to look-arounds, check out [Rexegg's guide to mastering look ahead and look behind](http://www.rexegg.com/regex-lookarounds.html)

The syntax looks like so:

Type

Syntax

Example

Look Ahead

`(?=query)`

`\d+(?= dollars)` matches 100 in "100 dollars"

Negative Look Ahead

`(?!query)`

`\d+(?! dollars)` matches 100 if it is NOT followed by the word "dollars"

Look Behind

`(?<=query)`

`(?<=lucky )\d` matches 7 in "lucky 7"

Negative Look Behind

`(?<!query)`

`(?<!furious )\d` matches 7 in "lucky 7"

### ==Abusing look-arounds to enhance conditionals==

In our conditional, we can only query the existence of groups that have already been set. Normally, this means that content of the group has been consumed and isn't available to the conditional.

But ==you can use a look-ahead to set a group without consuming any characters==! Is your mind blown yet?

Remember this code that didn't work?

```
"100USD".match(/(USD)(?(1)\d+)/) # nil
```

If we modify it to capture the group in a look-ahead, it suddenly works fine:

```
"100USD".match(/(?=.*(USD))(?(1)\d+)/)
=> #<MatchData "100" 1:"USD">
```

Let's break down that query and see what's going on:

-   `(?=.*(USD))` Using a look-ahead, scan the text for "USD" and capture it in group 1
-   `(?(1)` If group 1 exists
-   `\d+` Then match one or more numbers

Pretty neat, huh?
#paste/e 