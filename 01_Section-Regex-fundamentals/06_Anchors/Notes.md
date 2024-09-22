## Anchors (`^` & `$`)
* Anchors in regular expressions are special characters that specify positions within a string rather than matching actual characters. They are used to match the position before, after, or between characters in a string, ensuring that a pattern is found only in specific locations.

### Common Anchors in Regex :
  1. ****`^ (Caret) Anchor:`**** Matches the beginning of a line or string.

    Example: ^abc matches "abc" only if it appears at the start of the string.

  ****Note : In a multi-line string with the m (multiline) flag, ^ will match the start of each line.****

  2. ****`$ (Dollar) Anchor:`**** Matches the end of a line or string.

    Example: abc$ matches "abc" only if it appears at the end of the string.
    
  **Note : In a multi-line string with the m flag, $ will match the end of each line.**

  3. **`\b (Word Boundary):`** Matches a word boundary position between a word character `(\w)`.

    Example: \bword\b matches "word" as a whole word but not "worded" or "sword".

  **Note : Word boundaries are useful for matching entire words and avoiding partial matches.**

  4. **`\B (Non-Word Boundary):`** Matches a position that is not a word boundary.

    Example: \Bword matches "sword" but not "word" at the beginning of a string.