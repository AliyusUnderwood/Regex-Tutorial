# Regex Tutorial: Matching an Email

Regular expressions (regex) are powerful tools for matching patterns in text. In this tutorial, we'll break down the components of a regex for matching email addresses, so you can understand how it works and adapt it for your own use.

## Summary

The regex we'll be exploring is: `^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$`

This regex matches email addresses that meet the following criteria:
- Lowercase letters a-z, numbers 0-9, underscores, periods, or hyphens before the @ symbol
- A domain name after the @ containing lowercase letters, numbers, periods, or hyphens
- A dot followed by 2-6 lowercase letters for the top-level domain

## Table of Contents

1. [Anchors](#anchors)
2. [Quantifiers](#quantifiers)
3. [Character Classes](#character-classes)
4. [Grouping and Capturing](#grouping-and-capturing)
5. [Bracket Expressions](#bracket-expressions)
6. [Greedy and Lazy Match](#greedy-and-lazy-match)
7. [About the Author](#about-the-author)

## Regex Components

### Anchors

The anchors used in this regex are `^` and `$`.
- `^` matches the start of the string. Placing this at the beginning ensures that the string matches this pattern from the very start.
- `$` matches the end of the string. Placing this at the very end ensures that the string ends after matching this pattern.

### Quantifiers

Quantifiers in this regex include `+` and `{2,6}`.
- `+` matches the preceding token between one and unlimited times. It's used after `([a-z0-9_\.-]` and `([\da-z\.-]` to allow any number of the included characters before the @ and in the domain name.
- `{2,6}` matches the preceding token between 2 and 6 times. It's used to limit the top-level domain to between 2 and 6 lowercase characters.

### Character Classes

The character class `\d` is used in this regex. It matches any digit character, which is identical to `[0-9]`.

### Grouping and Capturing

Capturing groups are defined using parentheses `()`. This regex has 3:
1. `([a-z0-9_\.-]+)` matches the user email name before the @ symbol
2. `([\da-z\.-]+)` matches the email domain name after the @ symbol
3. `([a-z\.]{2,6})` matches the top-level domain after the dot

### Bracket Expressions

There are three bracket expressions in this regex:
- `[a-z0-9_\.-]` matches any lowercase letter a-z, number 0-9, underscore, period, or hyphen
- `[\da-z\.-]` matches any digit, lowercase letter a-z, period, or hyphen
- `[a-z\.]` matches any lowercase letter a-z or period

### Greedy and Lazy Match

The quantifiers `+` and `{}` are greedy, meaning they will match as many characters as possible. There are no lazy quantifiers used in this regex.

### About the Author

Aliyus Underwood is a nursing worker trying to learn coding. He's currently a coding student at the University of Oregon completing a full-stack developer certification.

GitHub: [AliyusUnderwood](https://github.com/AliyusUnderwood?tab=repositories)
