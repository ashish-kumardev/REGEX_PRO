# Lookaheads and Lookbehinds in Regex

**Lookaheads** and **Lookbehinds** are zero-width assertions in regex, meaning they match a position rather than actual characters. They allow you to look ahead or behind a pattern without including it in the match.

## 1. Lookaheads

Lookaheads assert that a certain pattern must follow the current position. There are two types:

### Positive Lookahead `(?=...)`

- Matches if the pattern inside the lookahead **exists** after the current position.
```
  Pattern : pattern1(?=pattern2)

  Example : Match only timing numbers.
  - 10 people can do a task in 4 hours.
  - 20 people can do a task in 2 hours.
  - 1 people can do a task in 28 minutes.
  - 2 hour
  - 1 min

  Pattern : /\d+(?= (?:hours?|min))/g
```

### Negative Lookahead `(?!...)`

- Matches if the pattern inside the lookahead **does not exist** after the current position.
```
  Pattern : pattern1(?!pattern2)

  Example : Match only timing numbers.
  - 10 people can do a task in 4 hours.
  - 20 people can do a task in 2 hours.
  - 1 people can do a task in 28 minutes.
  - 2 hour
  - 1 min

  Pattern : /\d+(?! people)\b/g
```

## 2. Lookbehinds

Lookbehinds assert that a certain pattern must precede the current position. There are two types:

### Positive Lookbehind `(?<=...)`

- Matches if the pattern inside the lookbehind **exists** before the current position.
```
  Pattern : (?<=pattern1)pattern2

  Example : Match only number with `$` sign.
  My name is ashish kumar and i have an $10 with  $5 extra so total is $15. But my friend have 20 dollars.

  Pattern : /\b(?<=\$)\d+/g
```

### Negative Lookbehind `(?<!...)`

- Matches if the pattern inside the lookbehind **does not exist** before the current position.
```
  Pattern : (?<!pattern1)pattern2

  Example : Match number without `$` sign.
  My name is ashish kumar and i have an $10 with $5 extra so total is $15. But my friend have 20 dollars.

  Pattern : /\b(?<!\$)\d+/g
```

## Notes

- Lookaheads and lookbehinds are **zero-width**, meaning they don't consume characters.
- Not all regex engines support lookbehinds, especially variable-length ones.
- We can write one or more than one lookaheads or lookbehinds

Use these patterns to match text based on context without including that context in the final match.
