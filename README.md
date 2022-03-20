# What is "REGEX"
​
As a full stack Developer I want to know what is "regex" and how it can be used to help benefit me in my day to day when needed, to do this we need to understand how we can use it as a tool for recognizing search patterns and how to implement it effectively 
​
## Summary
​
Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.
​
## Table of Contents
​
- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)
​
## Regex Components


### Anchors

​​  1.    /^abc$ -^start / $end of the string

2.   ^ Matches the beginning of the string, or the beginning of a line if the multiline flag (m) is enabled.This matches a position, not a character.
$ Matches the end of the string, or the end of a line if the multiline flag (m) is enabled. This matches a position, not a character.
\b\B -word, not-word boundary

\b Matches a word boundary position between a word character and non-word character or position (start / end of string). See the word character class (w) for more info.
\B Matches any position that is not a word boundary. This matches a position, not a character.
See Boundaries for more detailed Information
### Quantifiers

Indicate numbers of characters or expressions to match.
​
### Grouping Constructs

Grouping constructs delineate the subexpressions of a regular expression and capture the substrings of an input string. You can use grouping constructs to do the following:

Match a subexpression that is repeated in the input string.

Apply a quantifier to a subexpression that has multiple regular expression language elements. For more information about quantifiers, see Quantifiers.

Include a subexpression in the string that is returned by the Regex.Replace and Match.Result methods.

Retrieve individual subexpressions from the Match.Groups property and process them separately from the matched text as a whole.
​
### Bracket Expressions

A bracket expression enclosed in square brackets is a regular expression that matches a single character, or collating element. If the initial character is a circumflex ^, then this bracket expression is complemented.

See Character Class to see some examples.

​
### Character Classes

Consider a practical task – we have a phone number like "+7(903)-123-45-67", and we need to turn it into pure numbers: 79031234567.

To do so, we can find and remove anything that’s not a number. Character classes can help with that.

A character class is a special notation that matches any symbol from a certain set.

Most used are:

- \d (“d” is from “digit”)
A digit: a character from 0 to 9.
- \s (“s” is from “space”)
A space symbol: includes spaces, tabs \t, newlines \n and few other rare characters, such as \v, \f and \r.
- \w (“w” is from “word”)
A “wordly” character: either a letter of Latin alphabet or a digit or an underscore _. Non-Latin letters (like cyrillic or hindi) do not belong to \w.
​
### The OR Operator

When attempting to build a logical “or” operation using regular expressions, we have a few approaches to follow. Fortunately the grouping and alternation facilities provided by the regex engine are very capable, but when all else fails we can just perform a second match using a separate regular expression – supported by the tool or native language of your choice.
​
### Flags

Home > Courses > JavaScript RegExp > Foundation - Flags
JavaScript Regex Flags
What will you learn in this page?
What are flags
The ignore casing i and global g flags
The dot all s and multiline m flags
The sticky s flag
The unicode u flag
 
Foundation
Find and Highlight Exercise
Foundation
Flags Quiz
 
Introduction
In the previous chapter we got a fairly decent introduction to the syntax of a regular expression in JavaScript, and it is now that we will take it on from there to explore the bits and pieces in more detail.

In this chapter we shall begin with an understanding of what are flags in the world of regular expressions and how they can be used to modify the searching behaviour of given patterns. Once we're done, we'll test our skills at JavaScript Regex Flags Quiz.

Of all the flags detailed here, you'll find only the i and g flags to be easily understandable, since the others require concepts that we'll learn later in this tutorial.

Anyways, let's dive right into it.

What are flags?
We'll start by defining what exactly is a flag:

A flag is an optional parameter to a regex that modifies its behavior of searching.
A flag changes the default searching behaviour of a regular expression. It makes a regex search in a different way.

A flag is denoted using a single lowercase alphabetic character.

In JavaScript regex, we have a total of 6 flags, each serving a different purpose.

Flag	Name	Modification
-   i:	Ignore Casing	Makes the expression search case-insensitively.
-   g:	Global	Makes the expression search for all occurrences.
-   s:	Dot All	Makes the wild character . match newlines as well.
-m:	Multiline	Makes the boundary characters ^ and $ match the beginning and ending of every single line instead of the beginning and ending of the whole string.
-   y:	Sticky	Makes the expression start its searching from the index indicated in its lastIndex property.
-   u:	Unicode	Makes the expression assume individual characters as code points, not code units, and thus match 32-bit characters as well.
​
### Character Escapes

The backslash in a regular expression precedes a literal character. You also escape certain letters that represent common character classes, such as \w for a word character or \s for a space. The following example matches word characters (alphanumeric and underscores) and spaces.
​
## Author

Eoín Harkin