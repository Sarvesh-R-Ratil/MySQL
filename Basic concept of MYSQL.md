FLOOR(): This function rounds down the average population to the nearest integer.
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
The first condition checks if the sum of any two sides is less than or equal to the length of the third side. If true, 
it means the values do not form a triangle, hence the output is 'Not A Triangle'.
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
ORDER BY RIGHT(Name, 3), ID: This orders the output first by the last three characters of each student's name (RIGHT(Name, 3)), 
and then by ascending ID (ID) in case of a tie. The RIGHT function extracts the rightmost three characters of each name.

-----------------------------------------------------------------REGEXP only availabel in MySQL----------------------------------------------------------

Regular expressions, often abbreviated as regex or regexp, are a powerful tool for matching patterns in strings. They provide a flexible and concise way to search, extract, and manipulate text based on patterns of characters. Regular expressions are supported in many programming languages, text editors, and database systems.

Here's a breakdown of key components and concepts related to regular expressions:

Literal Characters: Regular expressions can include literal characters that match themselves. For example, the regular expression hello will match the string "hello" exactly.

Metacharacters: Metacharacters are special characters in regular expressions that have a specific meaning. Some common metacharacters include:

. (dot): Matches any single character except newline.
^: Matches the start of a string.
$: Matches the end of a string.
*: Matches zero or more occurrences of the preceding character or group.
+: Matches one or more occurrences of the preceding character or group.
?: Matches zero or one occurrence of the preceding character or group.
\: Escapes special characters, allowing them to be treated as literals.
Character Classes: Character classes allow you to match a set of characters. They are specified within square brackets [ ]. For example:

[abc]: Matches any of the characters 'a', 'b', or 'c'.
[a-z]: Matches any lowercase letter from 'a' to 'z'.
[^abc]: Matches any character except 'a', 'b', or 'c'.
Quantifiers: Quantifiers specify how many times a character or group should be repeated. Some common quantifiers include:

{n}: Matches exactly n occurrences.
{n,}: Matches at least n occurrences.
{n,m}: Matches between n and m occurrences.
*, +, ?: Greedy quantifiers that match as many characters as possible.
Anchors: Anchors are used to specify positions in the string. The ^ anchor matches the beginning of a line, and the $ anchor matches the end of a line.

Grouping: Parentheses ( ) are used to create groups within a regular expression. Groups can be used to apply quantifiers to multiple characters or to capture substrings for later use.

Alternation: The pipe symbol | is used to specify alternatives. For example, cat|dog matches either "cat" or "dog".

Escape Sequences: Regular expressions support escape sequences for matching special characters like newline \n, tab \t, etc.
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
