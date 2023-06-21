# Regex Tutorial

This is a tutorial on Regex.

## Summary

In this tutorial we will be explaining the regex functions, bit by bit. Breaking it down into smaller parts and explaining what each does.

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

This is a regex pattern and it is used to match and validate email addresses.
Here's a Javascript(Js) code to check if an email addres matches the pattern: 

const emaiRegex = /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/;

const email = "example@email.com";
if (emailRegex.test(email)) {
    console.log("Valid email address");
} else {
    console.log("Invalid email address");
}

## Table of Contents

- [Regex Tutorial](#regex-tutorial)
    - [Summary](#summary)
    - [Table of Contents](#table-of-contents)
    - [Regex Components](#regex-components)
        - [Anchors](#anchors)
        - [Quantifiers](#quantifiers)
        - [Or Operator](#or-operator)
        - [Character Classes](#character-classes)
        - [Flags](#flag)
        - [Grouping and Capturing](#grouping-and-capturing)
        - [Bracket Expressions](#bracket-expressions)
        - [Greedy and Lazy Match](#greedy-and-lazy-match)
        - [Boundaries](#boundaries)
        - [Back-references](#back-references)
        - [Look-ahead and Look-behind](#look-ahead-and-look-behind)
    - [Author](#author)    

## Regex Components

### Anchors

In regex, the anchor is represented by the '^' and the '$' symbols.

'^' represents the start anchor and the start of a string.
'$' represents the end anchor and the match should end at the end of the string.

These anchors make sure that the string is matched by Regex. So the pattern must match the enitre address not only part of it.

### Quantifiers

'+' this is a quantifier that indicates the preceding element should occur one or more times.

for example: '([a-z0-9_\.-]+)' matches one or more lowercase letters, digits, underscores, dots, or dashes. 

'{2,6}': it is a quantifier that specifies a range of occurrences for the preceding element.
in this case, '([a-z\.]{2,6})' matches between 2 and 6 lowercase letters or dots. 
It ensures that the top-level domain part of the email address has a length beween 2 and 6 characters.

### OR Operator

In the regex we do not have a Or Operator, but gennerally a Or Operator is represented by '|' It's used to indicate multple alterative patterns within a single group of subexpression. The Or Operator allows your regex to match any one of the provided patterns.

### Character Classes

Caracter classes are denoted by square bracktes and provide a way to define a range or a set of characters that can match a single position in the input string.
Here are the character classes used in the regex:

- '[a-z0-9_\.-]': this one matches a single character that can be a lowercase letter, a digit, an underscore, a dot, or a dash.
  It allows for a wide range of valid characters for the username and domain name parts of the email address.
- '[\da-z\.-]': this character class matches a single character that can be a digit, a lowercase letter, a dot, or a dash.
  The '\d' represents any digit, It is used in the domain name part of the email address.
- '[a-z\.]': this character class matches a single lowercase letter or a dot. I is used in the top-level domain part of the email address

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author
[Nestor Montanez](https://github.com/Nuno0123)
