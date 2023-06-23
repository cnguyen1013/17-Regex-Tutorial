# Regular Expression - Matching an Email

Regular expression matching is a powerful tool in the realm of text manipulation and pattern recognition, and one common application is validating and extracting email addresses. When it comes to efficiently and accurately verifying whether an input string adheres to the syntax of a valid email address, regular expressions provide a concise and flexible solution. By leveraging a well-crafted regular expression pattern, developers can easily perform email validation, ensuring that user input meets the required format for successful communication. Whether you're building a form validator or implementing email-related functionality, understanding regular expression matching for emails is an essential skill in the world of web development.

## Summary

This tutorial will be covering the regex expression used for both matching and validating an email:

`^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$`

The provided regex pattern is designed to validate the format of an email address. It ensures that the email address begins with one or more word characters, followed by an "@" symbol, then another sequence of one or more word characters separated by dots. The pattern concludes by requiring a dot followed by one or more word characters at the end of the email address. This regex pattern provides a basic level of validation but does not guarantee the actual existence or deliverability of the email address.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

The regex components that define this particular expression are anchors, quantifiers, meta escape characters, character classes, single character matches, grouping and capturing, and bracket expression. Regarding the example used in this tutorial: `^` and `$` are the anchors used, `+` and `{2, 6}` are the two quantifiers, `\d` represents the meta escape character utilized, `[a-z0-9_\.-]`, `[\da-z\.-]`, and `[a-z\.]` represent the character classes, `_`, `\.`, `-` represent the single character matches used, `()` represents the way this regex expression utilizes grouping and capturing, and `[]` delinates the bracket expression used.

### Anchors

Anchors within regex mark the start and end points of the expression. In regards to this expression, the `^` marks the start of the expression and the `$` marks the end of the expression. 

### Quantifiers

Quantifiers are meta characters that modify the previous character in the regex and say, how many of those do I want to match in a row.

Quantifiers allow the specification of how many character or character classes should be matched.

- The `+` sign matches one or more preceeding character
- `{min, max}` create a specific numerical quantifier range (you will notice this is used at the end of the regex expression     above at the end to give a specific range to the domain name system)

### Grouping Constructs

`()` creates a sequence or sub expression and is a way to treat multiple characters as a single unit. You will notice the regex expression being covered in this tutorial uses `()` to distinct groups of characters. The first set covers all characters before the `@` symbol. The second group coveres all characters before the `.`, and the last group covers all characters from the `.` to the end.

### Bracket Expressions

`[]` create a character or group range and represent a single character. In regards to the regex expression this tutorial is covering, the brackets are used to separate each character class. The character can be anything specified within the brackets.

Example: `[a-z0-9_\.-]` -> this character can be matched with any lowercase letters from `a-z`, and digit from `0-9`, an underscore `_`, a period `.`, or a dash `-`. 

### Character Classes

Character classes are the attribute in a regex expression that allow us to define specific sets of characters that can be used in a search pattern.

The character classes utilized in this regex expression are `[a-z0-9_\.-]`, `[\da-z\.-]`, and `[a-z\.]`.

`[a-z0-9_\.-]`: `a-z` matches a single character in the range between a (index 97) and z (index 122) (case sensitive), `0-9` matches a single character in the range between 0 (index 48) and 9 (index 57) (case sensitive), `_` matches the character _ with index 9510 (5F16 or 1378) literally (case sensitive), `\.` matches the character . with index 4610 (2E16 or 568) literally (case sensitive), and `-` matches the character - with index 4510 (2D16 or 558) literally (case sensitive).

`[\da-z\.-]`: `\d` can be used to match any digit (0-9), `a-z` matches a single character in the range between a (index 97) and z (index 122) (case sensitive), `\.` matches the character . with index 4610 (2E16 or 568) literally (case sensitive), and `-` matches the character - with index 4510 (2D16 or 558) literally (case sensitive).

`[a-z\.]`: `a-z` matches a single character in the range between a (index 97) and z (index 122) (case sensitive), and `\.` matches the character . with index 4610 (2E16 or 568) literally (case sensitive)

Other examples of single characters:

`\d` can be used to match any digit (0-9), `\w` to match any alphanumeric character (a-zA-Z0-9), and `\s` any white space such as a space or a tab

### The OR Operator

There are no OR operators within this particular regex expression but in general OR operators are represented with the pipe `|` and specified under the regex type of alternation.

### Flags

Regex flags are used to modify an expressions behavior -> case sensitivity, etc. There are only 6 of them in JavaScript -> i: case-sensitivity, g: looks for all matches, m: multiline mode, s: enables "dotall" mode that allows a dot `.` to match a newline character `\n`, u: enables full Unicode support, and y: "sticky" mode. 

The regex expression covered in this tutorial does not utilize flags.

### Character Escapes

Character escapes are used to match specific characters with special meanings or to represent certain character classes. The backslash followed by a dot (\.) is used to escape the dot character. The backslash followed by a hyphen (\-) is similar to the dot. The backslash followed by the letter "w" (\w) represents a shorthand character class for word characters. It matches any alphanumeric character (a-z, A-Z, 0-9) as well as the underscore character. 

## Author

Callistus Nguyen is a highly motivated individual with a deep passion for technology and innovation. With a background in biomedical engineering, Callistus constantly seeks opportunities to expand his knowledge and skills in various domains within the tech industry. He currently resides in Houston, TX.

Have additional questions? Click the links below to reach Callistus through his GitHub account or Email address.

[Link to Github](https://github.com/cnguyen1013)

<a href="mailto:cnguyen7@mdanderson.org">cnguyen7@mdanderson.org</a>