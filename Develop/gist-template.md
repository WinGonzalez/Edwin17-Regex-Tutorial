# Regex-Walkthrough
This tutorial introduces the intricacies of regular expressions, or regex for short. Throughout this guide, we will delve into the different elements that compose regex patterns, offering comprehensive explanations and practical examples to enhance your understanding of their functionality.

## Summary

In this guide, we will explore the complex world of regular expressions. Our journey will include an examination of key components including anchors, quantifiers, the OR operator, character classes, flags, as well as concepts of grouping and capturing, bracket expressions, both greedy and lazy matching techniques, boundaries, back-references, and the advanced look-ahead and look-behind mechanisms.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors
Anchors, symbolized by "^" for the start and "$" for the end, are used to assert particular positions within the text being searched. The caret "^" specifies that the matching should begin at the start of a line, while the dollar sign "$" indicates that the matching should conclude at the end of a line. These markers are crucial for confirming that the regex pattern matches the entire input from beginning to end.

Example:

Input: john.doe@example.com Explanation: The "^" anchor guarantees that the matching process commences right at the start of the string.

### Quantifiers
Quantifiers in regular expressions are used to define how many times the element preceding them should appear. The most common quantifiers include "+" for one or more times, "*" for zero or more times, "?" for zero or one time, "{n}" for exactly n times, "{n,}" for at least n times, and "{n,m}" for a range of n to m times.

"+" signifies one or more occurrences.
"*" indicates zero or more occurrences.
"?" denotes zero or one occurrence.
"{n}" requires exactly n occurrences.
"{n,}" allows for n or more occurrences.
"{n,m}" specifies a range from n to m occurrences.
Example:

Input: john.doe123@example.com
Explanation: Utilizing the "+" quantifier, the pattern matches one or more occurrences of alphanumeric characters preceding the "@" symbol.

### OR Operator
OR Operator The "|" symbol serves as the OR operator in regular expressions, offering a choice between the pattern on its left or right. For instance, "a|b" can match either 'a' or 'b'.

Example:

Input: john.doe@example.com or jane_doe@example.com Explanation: Using the OR operator "|", the regex can match a period (.) or an underscore (_) in the email username.

### Character Classes
Character Classes Defined within square brackets "[]", character classes match any one character from a specified set, useful for matching character ranges or specifying exceptions.

"[aeiou]" matches any vowel. "[0-9]" matches any digit. "[a-zA-Z]" matches any letter regardless of case. Example:

Input: john.doe123@example.com Explanation: The character class "[a-zA-Z]" matches letters in the email's domain part.

### Flags
Flags Regex flags like "/i" for case insensitivity, "/g" for global matches, and "/m" for multi-line matches, alter how patterns match text.

Example:

Input: john.doe@example.com Explanation: Flags would modify search behavior but aren't applied in this example.

### Grouping and Capturing
Grouping and Capturing Using parentheses "()", parts of a regex pattern can be grouped for capturing, allowing for extraction of specific data segments.

"([a-z]+)" captures a sequence of lowercase letters. Example:

Input: john.doe@example.com Explanation: "([a-z]+)" captures "john" as a group in the email username.

### Bracket Expressions
Bracket Expressions Like character classes but with more versatility, bracket expressions "[ ]" match one character from a defined set, including negations and ranges.

"[a-z]" matches any lowercase letter. "[^0-9]" matches any non-digit character. Example:

Input: john.doe@example.com Explanation: "[0-9]" matches digits in the username.
### Greedy and Lazy Match
Quantifiers are greedy by default, capturing as much as possible. A following "?" makes them lazy, aiming for the smallest match.

"." for greedy and ".?" for lazy matches.
Example:

Input: john.doe@example.com
Explanation: ".*" matches the entire local part of the email before the "@".

### Boundaries
The "\b" marker identifies word boundaries, ensuring matches at the start or end of words.

"\bword\b" precisely matches 'word'.
Example:

Input: word@example.com
Explanation: "\b" ensures "word" is matched as a distinct word.

### Back-references
Back-references like "\1" reference previously captured groups within the pattern, enabling matching of repeated sequences.

"(\w)\1" matches consecutive identical word characters.
Example:

Input: aa@example.com
Explanation: "(\w)\1" matches the repeating "aa" in the email username.

### Look-ahead and Look-behind
Assertions for look-ahead and look-behind "(?=...)", "(?!...)", "(?<=...)", "(?<!...)" set conditions for matching based on preceding or following text without including that text in the match.

Example:

Input: john.doe@example.com
Explanation: A look-ahead "(?=.)" could verify a dot is not the last character by ensuring it's followed by another character, optimizing the match in the email's local part.

## Author
My name is Edwin Gonzalez feel free to reach out! https://github.com/WinGonzalez




