# Regex Tutorial: Matching an Email

Hello, this is a Regex tutorial describing how to match an email address using a regular expression.

## Summary

I will break down and describe this specific regular expression:   
`` /^([a-z\d\.-]+)@([a-z\d-]+)\.([a-z]{2,8})$/ `` and how it can be used to match with an email.

These series of characters define a specific search pattern, and when included in code or search algorithms, this regex can be used to find an email address.

By end of this tutorial, I will explain how each specific character in this regular expression works.


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Character Escapes](#character-escapes)

## Regex Components

- A regular expression is considered a literal, so each regular expression much be wrapped in forward slash characters `` / ``.

### Anchors

- The characters `` ^ `` and `` $ `` are both considered anchors. The `` ^ `` anchor signifies a string that begins with the characters that follow it. 
- The `` $ `` anchor signifies a string that ends with the characters that precede it.

So in this regex, the string must start and end with something that matches this pattern:   
`` ([a-z\d\.-]+)@([a-z\d-]+)\.([a-z]{2,8}) ``

### Quantifiers  

- Quantifiers are identified by the characters wrapped in brackets `` {} ``. They set the limits of the string that your regex matches (or an individual section of the string). They usually include minimum and maximum number of characters.

- From our example: `` {2,8} ``. The quantifier suggests this part of the regex must contain at least 2 characters, but not more than 8 characters.

### Grouping Constructs

- Grouping constructs are used when regex grow more complicated. With grouping constructs you may check multiple parts of a string to determine that different sections fulfill different requirements. The primary way to group a section of a regex is by parentheses `` () ``.

- Here are the grouping constructs broken up from this regex:   
`` ([a-z\d\.-]+) ([a-z\d-]+) ([a-z]{2,8}) ``.   

- The grouping constructs are tied together with the `` + `` character.

### Bracket Expressions

- Anything inside a set of square brackets `` [] `` represents a range of characters that we want to match. These patterns are also known as a positive character group because they outline characters that we want to include.   

`` [a-z\d\.-] `` `` [a-z\d-] `` `` [a-z] ``   

- The first bracket `` [a-z\d\.-] ``suggests the regex will accept any letter from `` a-z ``, any digit from 0-9 `` \d ``, a period `` \. `` and the hyphen `` - ``.

- The second bracket `` [a-z\d-] `` suggests this regex will accept any letter from `` a-z ``, any digit from 0-9 `` \d ``, and the hyphen `` - ``.

- The third bracket `` [a-z] `` will only accept any letter from a to z.


### Character Classes

- A character class in a regex defines a set of characters, any of which can occur in a string to fulfill a match. Here are the character classes used in this regex:

- `` \d `` - this character class matches any numeric digit.
- `` [a-z] `` - this character class is case-sensitive and matches any letter from a to z.
- `` \. `` - this character class matches the period specifically. This class uses a character escape (`` \ ``) because the period by itself (`` . ``) matches any character, it is a wildcard.
- `` + `` -  this character is interpreted literally.
- `` @ `` - this character is interpreted literally as well. We are matching an email address so we need the `` @ `` symbol in-between the first 2 strings. we are checking in the regex.    
`` ([a-z\d\.-]+)@([a-z\d-]+) ``

### Character Escapes

- The backslash `` \ `` in a regex escapes a character that otherwise would be interpreted literally.
- In our example, the period `` . `` is used as a wildcard and will accept any value, but adding a backslash before the period `` \. `` means that the regex should look for the period `` . `` specifically, instead of any wildcard. This is common when looking for strings with special characters that are the same as a particular component of a regex.

## Author

[Justin Kemp](https://github.com/justinkemp10)

Currently a student in Northwestern's coding boot camp, looking for a career in coding!
