# Unpacking Matching a URL with Regex

A regular expression is defined as a sequence of characters that defines a search pattern for text. 
This tutorial will explain the various parts of regex as it pertains to matching with an email. 


## Summary

In this tutorial I will be breaking down the various parts of regex as it pertains to matching an email. 
Regex has many unique aspects that must be understood to decrypt its syntax. The bit of code that I will be unpacking looks as such:<br>
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`</br>


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
The `^` anchor identifies the beignning of the string. The `$` anchor identifies the end of the string. The characters between these two 
anchor tags are those which are to be matched with the pattern seen in 
a standard email address format. 
### Quantifiers
The + quantifiers that are seen following the bracket expressions containing the acceptable characters denote that there can be one or more of these characters present in the pattern.
The `{2,6}` quantifier that is found near the end of the expression signifies that between 2 and 6 characters included within the bracket expression to the immedate left of the quantifier can be included within the expression. 

### Character Classes
The `\d` that is present within the bracket expression after the `@` signifies a single character that is a digit. 

### Grouping and Capturing
The parentheses around each of the bracket expressions create a capturing group with the value of whatever is contained within the square brackets.

### Bracket Expressions
Bracket expressions are represented by square brackets, `[]` , and ultimately mean that the matched string can contain any of the characters allotted within the brackets. In the case of the email expression above that is being evaluated, the bracket expression closest to the beginning can be read as: `matches a string that can contain one or more of each of the following: letters a-z, digits 0-9, _ , . , or - `

### Greedy and Lazy Match
Greedy quantifiers work to repeat a character as many times as possible or specified. A lazy quantifier works to repeat a character as minimally as possible. The greedy quantifier is present in a couple of places within the email expression-- the `+` after the bracket expressions says to match the character/s within one or more times. The curly braces that are present in the final capture group works to include between 2 and 6 characters from the bracket expression to the immediate left. 

## Author
I am a Bootcamp Student at the UofArizona and burgeoning JavaScript enthusiast with my sights set on a career in web development. 
- [Garrett's GitHub Profile](https://github.com/gwarzecha)