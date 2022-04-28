# regex: matching email

Template for creating my first gist on Regex, or regular expressions are extremely useful tools organizing and working with data. In this tutorial we'll explain how a specific regular expression functions by breaking down each part of the expression and describing what it does and solve a real world problem.

## Summary

In this Tutorial you will learn how to use regex to MATCH an email, this solves a real world problem that happens in email validation that may be required for credential validation or for business operations such as sending email blasts. Regex uses patterns in text to solve problems. 

For most email addresses there is a general structure that is pretty standard `name@gmail.com`. The regex for matching email is: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`.  We are going to deconstruct this regex code to better understand how the code works. 

## Table of Contents

- [Preface](#preface)
- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Preface
This is a brief clarification to get started deconstructing our regex for matching email.
There are 2 ways to create a regex object. 
1. Literal Notation (which is our case): parameters are enclosed between slashes 
   Example: `/`^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$ `/`
3. Constructor Notation: where the functions perameters are inclosed between quotation marks 
   Example: `'`^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$ `'`

### Anchors
Anchor List: 
`^` `&`
Functionality: 
Anchors do not match any charactors, they are a parser to find or match a position of a string. For our example email validation use of regex, we know where the beging and end of the email address occurs because of the two anchors noted.  
Anchor Example: `^`name.gmail.com`$`
Anchor Code Snippet: 
/`^`([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})`$`/


### Quantifiers
Quantifier List: 
`*` `+` `?` `{a,b}`
Functionality: 
Quantifiers are sets of characters that indicate how many times qualifiying information can or must be repeated in the pattern. 
1. `*`  matches all of an empty string, predeeding element repoeated zero or more times 
2. `+` matches the preceeding element, so 🍎`+` is the same as 🍎🍎 and 🍎🍎🍎
3. `?` preceeding element is repeated zero or 1 time, so 🍎`?`🍊 is the same as 🍊 and 🍎🍊
4. `{a,b}` preceeding element is repeated at least a times, at most b times
Quantifier Example for email: name`+` @  gmail `+`.com
Quantifier Code Snippet: 
/^([a-z0-9_\.-]`+`)@([\da-z\.-]`+`)\.([a-z\.]{2,6})$/


### Grouping Constructs
Grouping List: 
`(` `)`
Functionality: 
If characters are to be grouped and treated as one group with parenthesis. In the snippet below you can see how an email address is grouped within the parenthesis. 
Grouping Example: `(` name `)` @ `(` gmail `)` . `(` com `)`
Grouping Code Snippet: 
/^`(`[a-z0-9_\.-]+`)`@`(`[\da-z\.-]+`)`\.`(`[a-z\.]{2,6}`)`$/

### Bracket Expressions
Bracket List: 
`[` `]`
Functionality: 
Bracket expressions means characters can be included or excluded if they match any charactor among those listed between the opening/closing square brackets.  
Braket Example: `[` name a-z (case sensitive) ,0-9 characters ._- `]` 

Braket Code Snippet: 
/^( `[` a-z0-9_\.- `]` +)@( `[` \da-z\.- `]` +)\.( `[` a-z\. `]` {2,6})$/

### Character Classes
Character Class List: 
a-z, 0-9 are alphanumberic 
0-9 numberic characters 
A-Z uppercase characters
a-z lowercase characters

Functionality: 
Character classes describe characters that have specific characteristics and can vary from country to country and they are only valid in the bracket expressions. 
Character Class Example: [`name is a-z(case sensitive),0-9 characters`] @gmail.com

Character Class Code Snippet: 
/^([ `a-z0-9_\.-` ]+)@([ `\da-z\.-` ]+)\.([ `a-z\.` ]{2,6})$/


## Author

I'm a very ambitious excited learner who is currently exploring full stack software development. I have a knowledge of many industries, professional experience in business operations including finance, legal, compliance and processes and enjoy learning new technologies to help businesses grow.

* My Github: https://github.com/AmyWilhoite
* My Gist: https://gist.github.com/AmyWilhoite
