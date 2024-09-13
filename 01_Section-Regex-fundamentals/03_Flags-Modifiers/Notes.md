## Flags or Modifiers

### Flags : 
* Flags in regex (regular expressions) are optional parameters that modify the way a pattern is interpreted by the regex engine. They can change the behavior of the search, making it case-insensitive, multi-line, etc.

#### Common Regex Flags:
* `g` (Global Search):
Searches for all matches in the text, not just the first one.

**Example: /cat/g will find all occurrences of "cat" in the text, not just the first one.**

* `i` (Case Insensitive):
Makes the regex search case insensitive.

**Example: /cat/i will match "Cat", "cAt", "CAT", etc.**

* `s` (Dot All Mode/Single line): Allows the dot (.) to match newline characters (\n). By default, `.` matches any character except newlines.

**Example: /a.b/s will match "a\nb" whereas without s, it would not.**

* `u` (Unicode): Enables full Unicode matching, allowing regex patterns to match any Unicode character correctly.
* \u{unicodeValue} with flag u: Pattern to write unicode regex.
* If we didn't use curly `{}` braces then we need to write full unicode value like : **\u0052**
* If we use curly `{}` braces then we didn't write to full unicode value like : **\u{52}**
* With the help of unicode we can search any type of character or any language character.

* **Note :** `This modifier not supported by all the browsers`. 

**Example: /\u{1F600}/u matches the Unicode character "😀" (grinning face emoji).**

* `y` (Sticky): Matches only from the last index where a previous match ended, rather than searching from the start. This is less common and is used in specific situations.
* When we use `y` flag it start from the start that it match or not and after that where the first match end the second match start again.

**Example: Using /cat/y with lastIndex set to 4 would only match "cat" if it starts exactly at position 4.**

**Note :** `m` flag is remain.