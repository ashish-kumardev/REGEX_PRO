## Delimiters, Literal Characters & Meta-characters

### Delimiters : 
* The characters between write regex is called delimiters.
* Characters are used in beginning and ending an regex, called as delimiters.
* Ex : /delimiters/ in JS.

### Literal Characters :
* The characters which behave same like they have called literal characters.
* Characters which have no special meaning called literal characters
* Ex : a-z, 0-9, A-Z

### Meta Characters :
* The characters which behave differently as they have.
* Characters with special meaning.
* Ex :  . ^ $ * + ? {} [] \ | ()

  #### `.` is a special meta-character and it matches any single character except newline characters (\n, \r).

  #### `\` is a special meta-character and it is used to remove/escape the specialty of special characters (\\\n, \\\t, etc.)

**Note : open and close curly braces `{}`, and close square bracket `]` match directly without using `\`.**