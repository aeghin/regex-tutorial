# Regex-tutorial 

In this tutorial of regular expressions, we'll cover the different components that makes a regex in detail.

## Summary

A regular expression is a sequence of characters that defines a search pattern for a body of text. Below is an example:

* URL - /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

An anchor doesn't match any characters. The purpose behind anchors is to match a position within the text before, or after a specific character. ("^" is for use of the begining of the text)("$" is for use at the end of the text). In the example above, you'll see /^(https?:\), indicating that the text coming back requires https?: to be at the begging of the url.

### Quantifiers

Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found. In the example above, /^(https?://)?([\da-z.-]+).([a-z.]{2,6})([/\w .-]*)*, the "*" indicates that it requires 0 or 1 more instance. if it were followed by a number, it would require that many more instances.

### Grouping Constructs

Grouping Constructs are used in regex to give different parts of a string different requirements. At the end of our email, for instance, since ([a-z\.]{2,6}) is within opening and closing parentheses, the 2-6 character rule will only apply to this section of code. This is used multiple times througout our regex to apply different specifications to different sections.

### Bracket Expressions

A bracket expression is either a matching list expression or a non-matching list expression. Our example, [a-z\.], matching any character a through z.

### Character Classes

Character classes distinguish kinds of characters such as, for example, distinguishing between letters and digits. In our example, \da-z, "/d' stands for matching one digit. So our expression requires at least 1 digit/character between a-z.

### The OR Operator

We do not use the OR Operator (|) in our code, but this can be used to esasentially apply bracket expression rules to other parts of the pattern, in that it will match with one requirement OR another, using | to separate character requirements.

### Flags

Flags are optional parameters that we can add to a plain expression to make it search in a different way. Each flag is denoted by a single alphabetic character, and serves different purposes in modifying the expression's searching behavior.

### Character Escapes

In general, the characters in a regular expression are taken literally in context of regular expressions. This can be avoided by using a backslash () before a character. While there are several 's in our expression, this rule does not apply for 's inside of bracket expressions. Therefore, the only example of a character escape in our code is \., indicating that we require a period in our string. The \ must be included, because a . on its own has its own specific meaning within regex.

## Author

https://github.com/aeghin
