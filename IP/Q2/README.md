2. Regular Expression and Various Functions

Definition
JavaScript provides regular expression capabilities through instances of the built-in RegExp object. A regular expression is a certain way of representing a set of strings. Regular expressions are frequently used to test that a string entered in an HTML form has a certain format, or, in the terminology of regular expressions, belongs to the set of strings that have the correct format.

Basic Example
The set of strings that consist of exactly three digits — which might represent, for example, the set of valid area codes in a phone number — can be represented by:

\d\d\d

Here, \d stands for the set of digit characters 0 through 9. Concatenating this string with itself three times represents the set of all possible strings of three consecutive digits.

Testing a Value
To check if a variable named areaCode contains exactly three digits:

var acTest = new RegExp(“ˆ\d\d\d$”);
if (!acTest.test(areaCode)) {
window.alert(areaCode + “ is not a valid area code.”);
}

The test() method of a RegExp instance returns true if its string argument is a member of the set of strings represented by the instance’s regular expression, otherwise false.

Literal Syntax
JavaScript provides an alternate syntax for creating a RegExp instance that avoids the need to duplicate backslashes.

For example:
var acTest = /ˆ\d\d\d/;

The expression on the right-hand side is known as a regular expression literal. The scripting engine converts such an expression to a call to the RegExp() constructor automatically escaping any backslash characters contained in it.

Special Characters
The special characters in JavaScript regular expressions are:

ˆ $ \ . \* + ? ( ) [ ] { } |

These characters must be escaped by a backslash to represent them literally. For example, $$ represents strings ending with a dollar sign.

Escape Codes
JavaScript provides several escape codes to match groups of characters:

\d – Digit: 0–9
\D – Any non-digit
\s – Whitespace (space, tab, line feed, etc.)
\S – Any non-whitespace
\w – Word character (letter, digit, underscore)
\W – Any non-word character

Operators in Regular Expressions

1. Concatenation – Joins patterns together. Example: ˆ\d.\w$ represents strings starting with a digit, followed by a period, a space, and ending with a word character.

2. Union (|) – Represents alternatives. Example: (+|-)\d|\s matches a plus or minus followed by a digit, or a whitespace.

3. Character Classes – Represent sets or ranges. Example: [a-z] matches lowercase letters.

4. Quantifiers – {n} means exactly n times, {n,m} means between n and m times, ? means 0 or 1 occurrence, \* means 0 or more occurrences (Kleene star), + means 1 or more occurrences.

Examples
• Range Matching: \d{3,6} matches any string of 3 to 6 digits.

• Optional Sign: (+|-)?\d matches an optional plus or minus followed by a digit.

• Password Example: A password that contains at least one digit, at least one letter, and may only contain digits, letters, and underscores can be represented by:
\w*(\d\w*[a-zA-Z]|[a-zA-Z]\w*\d)\w*

Summary
Regular expressions in JavaScript allow developers to define patterns for matching strings. They support features like special characters, escape codes, concatenation, union, character classes, and quantifiers. The RegExp object and test() method make it easy to check if input strings match desired patterns, which is especially useful for form validation, search operations, and text processing in client-side scripting

⸻
