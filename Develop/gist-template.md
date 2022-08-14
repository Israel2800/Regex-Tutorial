# Regex Tutorial, Matching a Hex Value

Regex or regular expressions are very useful in extracting information that is needed from any text, this is possible by searching specific patterns that are define as special characters.

## Summary

In this tutorial we will explain the usage of different components of a regular expression used to match Hex Values. The hexadecimal number system, also called base-16 or hex, is a number system that uses 16 unique symbols to represent an specific value, those symbols are 0-9 and a-f. This system will be used as a color code to express and match a specific color. We will be using the following regex:
```
/^#?([a-f0-9]{6}|[a-f0-9]{3})$/
```
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
In our regex we are using two anchors, which are:
`^` and `$`.
- The `^` represents a string that begins with the character that follow it. In this case the character used is `#`, that means that the hexadecimal color code must start with a `#` symbol.
- The `$` represents a string that ends with the characters that precede it, in our regex represents the end of the string.

### Quantifiers
The quantifiers will set the limit of the string that our regex matches. Most of the times they have included the minimum and maximum number of characters that the regular expression is looking for. In this regex we have the specific number of characters we are looking for. We have the following quantifiers:
- The `?` matches the pattern zero or one time.
- The `{6}` matches the pattern exactly `6` times, this represents the length of the component.
- The `{3}` matches the pattern exactly `3` times, this represents the length of the component.
As we can notice, we have to length components, this is because we have two types of formats, and we know this because of the `or` operator, which we will explain below.

### OR Operator
The `or` operator is represented with the character `|`. This operator indicates that it could be one or other of the two components we are separating with the `|` symbol. As we mentioned before, we have to types of formats, that is why we are using the `or` operator. This means that our first pattern either be `6` characters `[a-f0-9]{6}` or `3` characters `[a-f0-9]{3}`.

### Character Classes
The character classes will define a set of characters that we are expecting to match. In our case we are using character classes defined by the `[]` symbols. As we can see, it is implemented two times, which it means we have to character classes:
- `[a-f0-9]` and `[a-f0-9]`, they are looking for the same values, `a-f` stands for letter `a` to letter `f` and `0-9` stands for number `0` to number `9`.

### Grouping and Capturing
We are grouping our regex to capture information that we have inside of the `()` characters: 
- `([a-f0-9]{6}|[a-f0-9]{3})`, this also gives us organization when we want to add a component in our regex.

### Bracket Expressions
It is define as anything inside a set of square brackets `[]`, it will represent the range of characters that we want our regex to match, in our case we have the following information inside of the `[]` characters:
- `[a-f0-9]` and `[a-f0-9]`, they have the same parameters so they are looking to match the same values, such as `a-f` which is looking for letter `a` to letter `f` and `0-9` which is looking for number `0` to number `9`.

### Greedy and Lazy Match
In our regex we have the `?` character, which is considered a `lazy` quantifier, this because the `?` will allow as few matches as possible `(0 or 1 time)`. And a greedy component will try to match an element as many times as possible.

## Author
Hello everyone!, I am Israel Aguilar and I am currently studying the fundamentals to become a great full-stack web developer!
My GitHub: [Israel2800](https://github.com/Israel2800)