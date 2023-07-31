# Regex Tutorial

A README about Regular Expression.

## Summary

Regular Expressions (Regex) are tools for pattern matching and searching in strings. With this tutorial, I aim to demonstrate a widely used Regex. Validating email addresses. Email addresses use a common format: a string of characters, followed by a '@' symbol, another set of string characters, a period, and finally a domain.

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
The chosen Regex for this tutorial is:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

### Anchors

In regular expressions, anchors do not match characters but assert the position before or after characters. Our regex pattern begins with ^ and ends with $ which are the start and end of line anchors respectively. This means the pattern should match the entire string, not just a part of it.

### Quantifiers

Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found. In our regex, + and {2,6} are quantifiers. The + means "one or more" of the element should be present. {2,6} means between 2 to 6 of the preceding element should be found.

### Grouping Constructs

Grouping constructs () are a way to treat multiple characters as a single unit. Patterns inside a pair of round brackets are treated as a single unit and can be quantified, alternated, etc.

### Bracket Expressions

Bracket expressions [] define a character set, any one character enclosed within the set can be a match. In our case, [a-z0-9_\.-] and [a-z\.] are bracket expressions, which means we match any single character included in the set.

### Character Classes

In our regex, \d is a character class, which is a type of character set. \d matches any digit, it is equivalent to [0-9].

### The OR Operator

Our regular expression for validating email addresses doesn't contain an OR operator, but it's worth mentioning. The pipe | character represents the OR operator in regular expressions. It allows the regex to match one expression or another.

### Flags

Flags change the search behavior. They follow the closing slash of the pattern. Although our email validation regex doesn't include flags, it's important to note that flags such as g for global search, i for case-insensitive search are commonly used.

### Character Escapes

In our regular expression, \. is a character escape. It's used to match characters that have special meaning in regex syntax. The backslash \ is an escape character used before a special character we want to match.

## Author

This regex tutorial was written by Long Yang. My GitHub account is https://github.com/TojiCodes.
