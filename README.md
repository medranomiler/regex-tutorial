# regex-tutorial

Regular expressions, commonly known as regex, are utilized to detect patterns within text data. They have a wide range of applications, including searching and extracting data, validating data, cleaning and standardizing data, and manipulating and transforming text. Thus, regular expressions are an extremely adaptable tool.

## Summary

The regular expression "^[A-Za-z0-9.%+-]+@[A-Za-z0-9.-]+.[A-Za-z]{2,}$" has a specific purpose of validating email addresses. The beginning of the string is marked by the caret ^ anchor. The character class '[A-Za-z0-9.%+-]+' matches one or more occurrences of letters, digits, and special characters commonly found in email addresses. The @ symbol separates the local part of the email from the domain. The character class [A-Za-z0-9.-]+ matches letters, digits, and hyphens typically found in domain names. The period character is matched by the dot symbol, and in this instance, a forward slash is used as a character escape before it, as the period can also serve as a metacharacter. The character class [A-Za-z]{2,} matches two or more letters, which represent the top-level domain part of the email, such as .com or .edu. Lastly, the "$" anchor marks the end of the string.

## Anchors 
Anchors are categorized into two types: the caret (^) symbol and the dollar sign symbol ($). The caret symbol serves the purpose of locating a particular pattern, but only if it occurs at the beginning of a string. On the other hand, the dollar sign symbol locates a pattern at the end of a string.

## Quantifiers
Quantifiers are metacharacters used to determine the number of times a character, group, or class appears in a pattern. The asterisk symbol (*) matches zero or more occurrences of a character or group. In contrast, the plus sign (+) matches one or more occurrences of a group or character. A question mark symbol (?) matches zero or one occurrence of the preceding character or group. The curly brackets ({}) are used to match exactly the number of occurrences specified inside them. When there is a comma inside the curly brackets ({,}), it matches the number specified and more; for example, {5,} matches five or more occurrences. Curly brackets with a comma and two numbers inside ({2,3}) match the number of occurrences of the character or group between the two numbers specified.

## Grouping Constructs
Grouping constructs allow regular expression tokens to be grouped and treated as a single entity. This is useful as it allows quantifiers to be applied to the entire group, alternation to be applied to the group, or the matched text to be captured within the group. Capturing groups, which are created by placing a set of tokens inside a pair of parentheses (), capture the matched text into a numbered capture group that can be referenced later in the regex or in the replacement text of a search and replace operation. Non-capturing groups, which are created by placing a set of tokens inside a pair of parentheses followed by a question mark and colon (?:), do not create a numbered capture group. These groups are useful when you want to group a set of tokens without capturing the matched text.

## Bracket Expressions
Bracket expressions are used to define a set of characters that can match a single character in an input text. They are defined by enclosing a set of characters within a pair of square brackets ([]). Character ranges can be specified by placing a hyphen between two characters, for example, [a-z] or [1-9]. Additionally, you can include a caret (^) at the beginning, such as [^a-c], which matches any character that is not within the range of a-c, such as a, b, or c.

## Character Classes 
A character class is a set of characters that can be used to match any single character from that set. To define a character class, you can enclose the set of characters within a pair of square brackets ([]). Whatever characters are included inside the brackets will be matched with. In addition to specifying custom sets of characters, there are also predefined sets of common characters that can be used, such as \d which matches any digit character, \w which matches any alphanumeric character, and \s which matches any whitespace characters such as tabs or spaces.

## The OR Operator 
The OR operator in regular expressions is represented by the pipe symbol (|). It allows you to match one or more alternative patterns. You can use the OR operator to match one of several options, such as "white|black", which would match a string containing either "white" or "black".

## Flags
Flags are additional parameters that can help modify the behavior of regular expressions. They are added at the end of regular expressions.
"i"- ignore case, matches patterns without regard to case sensitivity. -"g": global, matches all occurances of a pattern, not just the first one. -"m": multiline, changes the behavior of "^" and "$" to match the beginnig and end of each line, rather than the beginning and end of the entire string. -"s": dotall, allows the "." metacharacter to match any character, including newlines. -"x": verbose, allows you to write regular expressions that are more readable by ignoring whitespace and comments.

## Character Escapes
A character escape is used to treat a character with a special meaning in a regular expression as a literal character instead. To use a character escape, you add a backslash () before the character with the special meaning, such as + or *. This is important when you need to match a specific character that has a special meaning in regex, but you want to use its literal meaning instead.


