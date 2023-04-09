# Regex-Tutorial

This Challenge is to create a Tutorial that explains how a specific regular expression, or regex, functions by breaking down each part of the expression and describing what it does. To complete this assignment we use Github Gist. 

## Summary

Regex is a series of special characters that define a search pattern. The following code will be used to give examples for how the components of regex can be used.


Matching an Email –

` /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ `

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors

The Anchor signifies a string that begins with the characheters that follow. 

` /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ `

Anchors inform us that the engine's current position in the string matches a determined location: for example, the beginning of the string/line, or the end of a string/line

The anchors are `^` and ` $ ` The code lets us know we're looking for something that starts with 

` ^([a-z0-9_\.-]+) `

and ends with

`.([a-z\.]{2,6})$`

It has to start and end with the given parameters, if not then it won't be a match. 


### Quantifiers

A Quantifier specifies how many instances of a character, group, or character class must be present in the input for a match to be found. For an example, if we used the following code in our regex, `dyz+` then it'll match any string dy followed by at least one z. With that, if we look at the code for matching the email: 

`([a-z0-9_\.-]+)`

this will match any string that contains `a-z,0-9, _, ., or -'. The +` means it contain at least one or more of this in order to have a match.

### OR Operator

The OR operator is not present in given email code, however we'll look at the following code for matching a hex code. 

` /^#?([a-f0-9]{6}|[a-f0-9]{3})$/ `

This regex matches a hex code that uses the OR Operator which will match where it starts with the `#` followed by :

`[a-f0-9]{6}` Then it'll match 6 charachter string containing a combo of a-f letters and 0-9 numbers.

`|` OR Operator

`[a-f0-9]{3}` which will match a 3 character long string that contains a combo of a-f letters and 0-9 numbers. 

### Character Classes
A character class in a regex defines a set of characters, any one of which can occur in an input string to fulfill a match.
'\d' is present in the given matching email code and it will match an Arabic numeral digit, after the @ sign in the email address. 

### Flags

Flags are placed at the end of a regex, after the second slash, and they define additional functionality or limits for the regex. A regex flag is not used in the matching email code that is being used for this tutorial. 

Examples of Flags are as follows:
* `g` - Global, does not return after the first match, which restarted any subsequest searches from the end of the previous match (Makes the expression search for all occurences)
* `m` - Multi-line, when enabled the Anchors (^ $) will match the start and end of a line, rather than the whole string
* `i` - Insensitive, makes the entire expression case-insensitive

### Grouping and Capturing

The primary way you group a section of a regex is by using parentheses (()).

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

`([a-z0-9_\.-]+)` is the first group that appears in our regex. This must be true before moving on to "match" the next part of the code. `([\da-z\.-]+)` is the second group that appears in our regex. `([a-z\.]{2,6})` lastly the third group that appears in our regex.

Grouping unifies a pattern or string so that it is matched in a complete block. 

### Bracket Expressions

Bracket Expressions are characters enclosed by a bracket `[]` matching any single character within the brackets.

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

In this case an example would be as follows :

`[a-z0-9_\.-]`

### Greedy and Lazy Match
Greedy and/or Lazy Matching are quantifies that expand the match as far as possible through the text. 
In the given code for matching an email, there isn't a greedy or lazy match included.

### Boundaries

Boundaries are described as the places between characters. A Boundary should be thought of as a wall between any adjacent characters.
There are two types of Boundaries, **Word** and ***Non-Word**, each denoted by a specific character.
* `\b` - A position that bounds a word, or where a word starts or ends.
* `\B` - Exact opposite of a word boundary, the negation of `\b` and will match **any position a word boundary doesnt.

### Back-references
Back-References identifies a previously matched group and looks for exactly the same text again. 
Back-references are not included in the given code.

### Look-ahead and Look-behind
Lookahead is useful for matching something depending on the context after it, and lookbehind- the context before it. If using a look-ahead or look-behind, then it has to match in a specific order. It is not being used in the given matching an email code.

## Author

Jazmin Traci Johnson 

If you have any questions about this repo, contact me directly at tracij50@gmail.com. You can find more of my work at Tracij1286 on Github https://github.com/Tracij1286 on Github.
