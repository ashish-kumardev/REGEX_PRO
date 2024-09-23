## Anchors (`^` & `$`)
* Anchors in regular expressions are special characters that specify positions within a string rather than matching actual characters. They are used to match the position before, after, or between characters in a string, ensuring that a pattern is found only in specific locations.

### Common Anchors in Regex :
  1. ****`^ (Caret) Anchor:`**** Matches the beginning of a line or string.

    Example: ^abc matches "abc" only if it appears at the start of the string.

  ****Note : In a multi-line string with the m (multiline) flag, ^ will match the start of each line.****

  2. ****`$ (Dollar) Anchor:`**** Matches the end of a line or string.

    Example: abc$ matches "abc" only if it appears at the end of the string.
    
  **Note : In a multi-line string with the m flag, $ will match the end of each line.**

  3. **`\b (Word Boundary):`** 
  * **Scenario 1 :** When we use ***word character class*** `\w [A-Za-z0-9_]` as a search pattern  then `\b` check there is no word character happen in right side if we add `\b` right side or left side if we add `\b` left side.
  
        Example: \bword\b matches "word" as a whole word but not "worded" or "sword".

  * **Scenario 2 :** When we use ***non-word character class*** `\W [^A-Za-z0-9_]`  then `\b` check there is a word character happen in right side if we add `\b` right side or left side if we add `\b` left side.

        Example : "/\b\w+\.?\w+?@\w+\.(?:com|in|org)/g" this regex exp. match only email which have .org .in & .com in the end.

        app.@gmail.in
        "info@gmail.com"
        @support.org
        "exmple@gmail.com"
        "app@support.com"
        "app.support12@gmail.in"
        "support@goole.org"

  **Note : Word boundaries are useful for matching entire words and avoiding partial matches.**

  4. **`\B (Non-Word Boundary):`**
  * **Scenario 1 :** When we use ***word character class*** `\w [A-Za-z0-9_]` as a search pattern  then `\B` check there is a word character happen in right side if we add `\B` right side or left side if we add `\B` left side.
  
        Example: \Bword matches "sword" but not "word" at the beginning of a string.

  * **Scenario 2 :** When we use ***non-word character class*** `\W [^A-Za-z0-9_]`  then `\B` check there is no word character happen in right side if we add `\B` right side or left side if we add `\B` left side.

        Example : "/\B@\w+\.(?:com|in|org)/g" this regex exp. match only email which have .org .in & .com in the end.

        "@#$#$@gmail.in"
        info@gmail.com
        "@support.org"
        exmple@gmail.com