## Character Classes

* Character classes in regular expressions are used to define a set of characters that you want to match in your pattern. They allow you to match one character out of a group of characters. Here's an overview of how character classes work and some common examples:

### Basic Character Classes
 1. ****Square Brackets[ ] :**** Defines a set of characters to match.

    * ****Example: ****[abc]**** matches any of a, b, or c.****


### ****Note : The range should be low ASCII value to high ASCII value****

 2. ****Ranges inside Character Classes:****

* ****[a-z]:**** Matches any lowercase letter.
* ****[A-Z]:**** Matches any uppercase letter.
* ****[0-9]:**** Matches any digit.

 3. ****Negated Character Classes [^ ]:****
 * Adding a `^` at the start negates the character class, matching anything not in the set.
 
    * ****Example: [^abc] matches any character except a, b, or c.****