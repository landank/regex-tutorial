# Regex-Tutorial: 

A regex, which is short for regular expression, is a sequence of characters that defines a specific search pattern. When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string. They are also frequently used to validate input.

Although they look daunting, this tutorial will break down hex Regex to show their value within the programing world. 

## Summary: Hex 

This expression matches HEX values.

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

Within this tutorial, the anchors, quantifiers, OR Operator, character classes, grouping and capturing, bracket expressions, and greedy/lazy match are broken down to better understand the usage of this Regex. 

This regex is able to match a hex values like: #a54, 555, abcdef, and others. 

The expression means the regex can match a hex value:
- With or without a # symbol
-  Any lowercase letter a-f 
-  Any number 0-9
- 3 or 6 characters long 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Author](#Author)

## Regex Components

### Anchors

Anchors aid in the search process by asserting information about the string. 

`^` anchor indicates what the string must begin with. 
Example: `^This` means the string must begin with `This`

`$` indicates what the string must finish with. 
Example: `End$` means the string must begin with `End`

IN THE HEX CODE EXAMPLE: `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`
The string has to match with the 3 or 6 character pattern identified before the `$` anchor. 

### Quantifiers

Quantifiers define how many times a character must be present in the match that is being searched for. 

`{n}` means that the character matches exactly `n` times. 
'?' means the preceding character is optional. 

IN THE HEX CODE EXAMPLE: `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`
`{6}` means the string will contain 6 characters. 
`?` means that the character `#` is optional.
`{3}` means that the string will contain 3 characters. 

### OR Operator

The OR operator, `|` or `[]` is a bolean that allows different paramaters to be allowed and/or searched for. 

IN OUR HEX CODE EXAMPLE: `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`
The OR operator means that our string will either have 3 or 6 characters. 

### Character Classes

Character classes define the characters that can be used. This is marked by the `-` character. 
IN OUR HEX CODE EXAMPLE: `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`
 `[a-f0-9]` means that the characters being searched for are lowercase a-f and 0-9. 

### Grouping and Capturing

By using the `()` character, grouping allows you to apply quantifiers to an entire group. 

IN OUR HEX CODE EXAMPLE: `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`
The grouping allows for the quantifier of `{6}` or {3} to be applied to all of the characters. 

### Bracket Expressions

Bracket expression matches a certain pattern of characters that is defined within brackets `[]`. 

IN OUR HEX CODE EXAMPLE: `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`
The brackets here indicate matching a string that has lowercase a-f or 0-9. 

### Greedy match and Lazy Match

Greedy Match is finding the longest possible string, while Lazy match means finding the shortest possible string. 

Normal quantifiers `{}` (quantifiers define how many times a character must be present in the match that is being searched for) are greedy. Although, if `?` was appended, the quantifier would become lazy. 

IN OUR HEX CODE EXAMPLE: `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/` 
The quantifier is greedy, meaning it wants to match as many digits as it can. 

## Author

I'm Landen Blankinship. I am a novice web developer intetested in front end design and user interface. I am trying to learn as much as I can so I am not stuck doing manual labor my whole life.
