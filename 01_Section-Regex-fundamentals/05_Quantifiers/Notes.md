## What is Quantifiers
* Quantifiers in regular expressions specify how many times the preceding element or left side (character, group, or character class) should occur in the input string for a match to be found. They are crucial for controlling pattern repetition in regex.

### Common Quantifiers
 1. ****`{n}:`**** Matches exactly `n` occurrences of the preceding element.

    * ****Example: a{3} matches 3 in given string : "aaa", "aaa`{zero character separate}`aaa".****

 2. ****`{n,}:`**** Matches `n` or more occurrences of the preceding element.

    * ****Example: a{3,} matches 2 in given string : "aaa", "aaaaaa".****

 3. ****`{n,m}:`**** Matches between `n` and `m` occurrences of the preceding element.

    * ****Example: a{1,3} matches "a", "aa", or "aaa".****

 4. ****`*` (Asterisk):**** Matches `0` or more occurrences of the preceding element.

    * ****Example: `a*` matches `"", "a"`, `"aa", "aaa"`, etc.****

 5. ****`+` (Plus):**** Matches `1` or more occurrences of the preceding element.

    * ****Example: `a+` matches `"a", "aa", "aaa"`, etc.****

 6. ****`?` (Question Mark):**** Matches `0` or `1` occurrence of the preceding element, making it optional.

      * ****Example: a? matches "" and "a".****

      