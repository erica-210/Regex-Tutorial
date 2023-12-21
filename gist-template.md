# Hex Value Regex Tutorial

Regex or Regular expressions, are tools for pattern matching in strings. In this tutorial we will explore the pattern made up to represent hex value code which is a hexidecimal representation of a color. 

## Summary

The regex `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/` checks if a string is a valid hex color code. It allows an optional `#` at the beginning, followed by either six characters or three depending on format type. This tutorial will break down the regex and explain each part's role in the overall pattern. 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors

Anchors are tokens that ensure your search expression matches a string at specific places. The carat `^` is set to match the beginning of a string and the dollar sign `$` marks the end of a string. In this instance, the `^` in conjunction with the `?` means a hex value has the option to start with a `#`. Meanwhile, the `$` signifies the string will end after the character limit within the matching character types have been met. 

### Quantifiers

Quantifiers are metacharacters that specifiy how many times a character, group, or character class should be matched. The question mark `?` and curly brackets `{}` are both quantifiers. The `?` means a character can be used zero to one time which is why the `#` is optional. The `{}` means the pattern must match the specified number of occurances allowed. In this case the pattern must be either six characters long `{6}` or three `{3}` depending on if the code is full format or short format.

### OR Operator

An or operator `|` literally means this or that. So for `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/` the hex code pattern can either be `[a-f0-9]` and six characters long OR `[a-f0-9]` and three characters long. 

### Character Classes

Character classes are a set of characters enclosed within square brackets `[]`. `[a-f0-9]` allows any lowercase letter 'a' through 'f' or any digit within the pattern. 

### Grouping and Capturing

In regex, grouping and capturing are used to extract information from text.  In this regex, parentheses `()` are a group expression. They group the full and short hex color code formats together, allowing the OR operator to apply to the entire group.

### Bracket Expressions

Bracket expressions in regex are a list of characters and/or character classes enclosed in square brackets `[]`. This is covered in character classes, but basically allow a range of characters for the patter. 

### Greedy and Lazy Match

'Greedy' means match longest possible string while 'Lazy' means match shortest possible string. In regex, greedy matches are the default behavior, while lazy matches are also known as non-greedy matching. In a hex value pattern we use greedy matching meaning we use as many characters as possible withing the length limit we are given for a valid color code. 

## Author

This tutorial was written by Erica San Miguel, a UTSA Bootcamp student. You can find more of my work on [GitHub](https://github.com/erica-210).
