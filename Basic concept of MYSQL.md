-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
The first condition checks if the sum of any two sides is less than or equal to the length of the third side. If true, 
it means the values do not form a triangle, hence the output is 'Not A Triangle'.
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
ORDER BY RIGHT(Name, 3), ID: This orders the output first by the last three characters of each student's name (RIGHT(Name, 3)), 
and then by ascending ID (ID) in case of a tie. The RIGHT function extracts the rightmost three characters of each name.

-----------------------------------------------------------------------REGEXP only availabel in MySQL----------------------------------------------------------------------------

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

Query the difference between the maximum and minimum populations in CITY.

select max(population)- min(population) as popdifference from city
how difference must be calculated
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
The main difference between the CEIL() and FLOOR() functions in MySQL lies in how they round numbers:
FLOOR(): This function rounds down the average population to the nearest integer.
CEIL(): The CEIL() function rounds a numeric value up to the nearest integer greater than or equal to the given value. In other words, it always rounds the number up to the next higher integer.

Example:

CEIL(3.14) returns 4 because 4 is the smallest integer greater than or equal to 3.14.
CEIL(9.5) returns 10 because 10 is the smallest integer greater than or equal to 9.5.
FLOOR(): The FLOOR() function rounds a numeric value down to the nearest integer less than or equal to the given value. In other words, it always rounds the number down to the next lower integer.

Example:

FLOOR(3.14) returns 3 because 3 is the largest integer less than or equal to 3.14.
FLOOR(9.5) returns 9 because 9 is the largest integer less than or equal to 9.5.
In summary:

CEIL() rounds up to the next higher integer.
FLOOR() rounds down to the next lower integer.
You would use CEIL() when you want to round a number up, and you would use FLOOR() when you want to round a number down.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
SELECT CEIL(AVG(Salary) - AVG(REPLACE(Salary, '0', ''))) AS ErrorAmount
FROM EMPLOYEES;

he REPLACE() function in MySQL is used to search for a specified substring within a string and replace it with another substring. In this context, REPLACE(Salary, '0', '') is used to remove any occurrences of the character '0' from the Salary column.

Let's break down the function:

Salary: This is the name of the column from which we want to remove zeros.
'0': This is the substring we want to search for within the Salary column. In this case, we are searching for the character '0'.
'': This is the replacement substring. Since we are not specifying any replacement string (empty string), the function effectively removes any occurrences of '0' from the Salary column.
For example, if we have a salary value of '20,000' in the Salary column, applying REPLACE('20,000', '0', '') would result in '2,'. The '0' is removed, and the remaining characters are left unchanged.

In the context of the previous query, AVG(REPLACE(Salary, '0', '')) calculates the average salary after removing any zeros from the Salary column, which is relevant for the calculation of the difference between Samantha's miscalculated and actual average salaries.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
SELECT ROUND(135.375, 2);
HERE ROUND WILL DEFINE TO 2 LAST DECIMAL POINT
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
TRUNCATE() Function:

The TRUNCATE() function is used to remove the decimal part of a numeric value, effectively truncating the number to a specified number of decimal places or integer part.
It simply removes the fractional part of the number without rounding.
Syntax: TRUNCATE(number, decimals)
Example:
TRUNCATE(3.145, 2) returns 3.14.
TRUNCATE(3.145, 0) returns 3.0.
In some SQL dialects, TRUNCATE() may behave differently. In MySQL, it truncates towards zero.
ROUND() Function:

The ROUND() function is used to round a numeric value to a specified number of decimal places.
It rounds the number based on a specified rounding rule (e.g., rounding up, rounding down, or rounding to the nearest integer).
Syntax: ROUND(number, decimals)
Example:
ROUND(3.145, 2) returns 3.15.
ROUND(3.145, 0) returns 3.0.
By default, ROUND() rounds to the nearest integer.
In summary:

TRUNCATE() removes the decimal part of a number without rounding.
ROUND() rounds a number to a specified number of decimal places based on a specified rounding rule.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

