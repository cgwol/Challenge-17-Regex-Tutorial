# Regex URL Tutorial

In this tutorial we will go over the regular expression, or Regex, for Uniform Resource Locators, or URLs. Regex's are powerful tools for defining specific search patterns within text. There are applications for regex's in a wide range of areas, from text processing to form validation. 

## Summary

In this tutorial, we'll explore the regular expression for matching a URL:

    /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

This regex pattern isused to validate and parse URLs. We are going to break down each component of this regex and explain what it does. 

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

Anchors are used to specify the position of a match within a string. In our URL regex, we use `^` and `$` as anchors to indicate the start and end of the string, ensuring that the URL is a complete match.

### Quantifiers

Quantifiers control how many times a character or group in the regex can appear. For example, `?` is used to make the `https://` part of the URL optional, and `*` allows for multiple path segments.

### OR Operator

The `|` symbol is the OR operator in regex. We do not use the OR operator in our regex but an exmaple is `/a|b/`. This regex allows only the input of characters `a` or `b`. 

### Character Classes

Character classes allow you to specify a range of characters that can match a particular position. In the URL regex, `[\da-z\.-]` matches any digit, lowercase letter, dot, or hyphen.

### Flags

Flags are used after the closing slash in regex and can modify how the expression behaves. For example, the `/i` flag makes the regex case-insensitive.

### Grouping and Capturing

Parentheses `()` are used to create capturing groups. In our regex, we use capturing groups to extract the protocol, domain, and path segments.

### Bracket Expressions
Bracket expressions allow you to specify a character from a defined set. In our URL regex, `[\/\w \.-]*` matches the path segment, which can contain letters, numbers, slashes, spaces, dots, and hyphens.

### Greedy and Lazy Match

The regex engine is greedy by default, meaning it will match as much as possible. In our regex, `*` is greedy. To make it lazy, use `*?` to match as little as possible.

### Boundaries

Boundaries are used to specify word boundaries. They are denoted by `\b`. In our URL regex, we don't use word boundaries. An example of boundaries is `\bapple\b`, the regex would search for the whole word `apple`.

### Back-references

Back-references allow you to match the same text that was captured by a capturing group. In our URL regex, we don't use back-references. An eample would be `(\d)\1`, `/d` is capturing digits while `\1` is the back refereance, which is checking for repeated digits. If it was capturing the the string `37729`, this regex would catch `77`.

### Look-ahead and Look-behind

Look-ahead and look-behind are used to assert that a particular pattern is (or isn't) ahead of or behind the current position. In our URL regex, we don't use look-ahead and look-behind. An exmaple of look-ahead is `\w+(?=\sapple)`. `\w+` matches one or more word characters while `(?=\sapple)` is a positive look-ahead assertion. It checks if there's a space followed by the word `apple` without including `apple` in the match.

## Author

This tutorial was created by [Christian Walterson](https://github.com/cgwol) as part of an assignment of UofM's full stack web development bootcamp
