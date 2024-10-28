# Alternation in Regex

Alternation in regex (regular expressions) allows you to match one pattern or another. It acts like a logical "OR" operator and is represented by the pipe symbol `|`. It’s useful when you want to match one of several possible options.

## Basic Syntax

`/pattern1|pattern2|pattern3/`

- `pattern1`, `pattern2`, and `pattern3` are the options you want to match.
- The regex engine will attempt to match each option from left to right.

## Example
If you have the following string: **apple banana cherry**

And you use the regex: `/apple|banana|cherry/`


The regex will match `apple`, `banana`, or `cherry` wherever they appear in the text.

## Grouping with Alternation
Alternation can be combined with parentheses for more complex patterns:
I like (cats|dogs)

This will match either `I like cats` or `I like dogs`.

## Important Note
The regex engine tries to match the options from ***left to right***, so if patterns overlap, the first match will be chosen. For example:

`/cat|cats/`

Given the string `I have cats`, the regex will match `cat` instead of `cats` because it appears first. To fix this, you can reorder them:

cats|cat

This way, the longer pattern (`cats`) is matched first.
