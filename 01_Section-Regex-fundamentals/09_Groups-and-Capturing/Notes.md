
# Groups and Capturing in Regex

Regular expressions (regex) provide powerful ways to match and capture parts of strings. Groups allow you to extract specific portions of a match and reuse them.

## 1. Capturing Groups

Capturing groups are defined using parentheses `( )`. The part of the pattern inside the parentheses is captured for use later.

**Syntax:** 
```
(pattern)
```

**Example:**
```regex
(\d{3})-(\d{2})-(\d{4})
```

This matches a sequence like `123-45-6789`. Each part of the sequence within parentheses is captured:

- `(\d{3})` captures the first three digits.
- `(\d{2})` captures the next two digits.
- `(\d{4})` captures the last four digits.

When used with a function like `.match()` in JavaScript.

- In JavaScript: `match[1]`, `match[2]`, etc.

## 2. Non-Capturing Groups

Non-capturing groups are used when you don't need to capture a part of the pattern. They are defined with `(?:...)`.

**Syntax:**
```
(?:pattern)
```

**Example:**
```regex
(?:\d{3})-(\d{2})-(\d{4})
```

This matches the same sequence as above, but only the second and third groups are captured. The first group is not captured, reducing memory usage if that part isn't needed.

## 3. Named Capturing Groups

Named capturing groups provide a way to assign names to groups, making it easier to reference them later.

**Syntax:**
```regex
(?<name>pattern)
```

**Example:**
```regex
(?<area>\d{3})-(?<middle>\d{2})-(?<end>\d{4})
```

Here, instead of accessing groups by number, you can access them by name:

- In JavaScript: `match.groups.area`

## 4. Backreferences

Backreferences allow you to reuse a previously captured group within the same pattern using `\1`, `\2`, etc., or by name.

**Example:**
```regex
(\w+)\s+\1
```

This matches any word followed by whitespace and the same word again (e.g., `hello hello`).

For named groups:
```regex
(?<word>\w+)\s+\k<word>
```

This does the same as the example above using the group name.
