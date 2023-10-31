# Understanding the Regular Expression: Matching a URL

## Summary

In this tutorial, we will explain a specific regular expression used to match a URL:  <span style="color: red;">/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/</span>. I will break down each component of the regex and describe its role in validating a URL.

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
- [Author](#author)

### Anchors

`^` and `$` are anchors that respectively match the start and end of the string. They ensure that the regex matches the entire string.

### Quantifiers

`?` matches the preceding character or group (in this case, the protocol) zero or one time. It makes the protocol part of the URL optional.
`*` matches the preceding character or group zero or more times. It allows for an optional path and query parameters.

### OR Operator

`https?` uses the `?` quantifier to make the "s" in "https" optional, allowing the regex to match both "http://" and "https://".

### Character Classes

`[a-z]`, `[0-9]`, and `[\da-z\.-]` define character classes to match lowercase letters, digits, and the characters allowed in the domain part of the URL.

### Flags

Flags, such as `i`, can be added to the regex to make it case-insensitive, allowing it to match `HTTP://` or `https://`.

### Grouping and Capturing

`()` is used for grouping in this regex. Groups capture portions of the URL, making it easier to extract and use specific parts of it.

### Bracket Expressions

`[\/\w \.-]` is a bracket expression defining a character set for matching characters in the path. It allows forward slashes, word characters, spaces, dots, and hyphens.

### Greedy and Lazy Match

`*` in `([\/\w \.-]*)*` is a greedy quantifier, matching as much as possible. It captures the entire path and query string.

### Boundaries

The `^` and `$` anchors enforce boundaries at the start and end of the string, ensuring the regex matches the whole URL.

### Back-references

This regex doesn't use back-references, but they are useful for matching repeated content, such as HTML tags with matching opening and closing tags.

### Look-ahead and Look-behind

This regex doesn't use look-ahead or look-behind as well.

## Author

This tutorial was created by Stanislav Bazeliuk. You can find more of my work on my GitHub profile - https://github.com/stasbaz
