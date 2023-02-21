# Regex-Tutorial
The term Regex stands for 'Regular Expression'. The regex is a sequence of different characters which describe the particular search pattern. It's a string of text that allows you to create patterns that help match, locate, and manage text.

## Summary
The Regex that I will be going over is matching an email address. I will be going into detail of the breakdown on this expression. Below is what the expression looks like:
 ```/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/```
 
 This works to match an email address within a sample of text, or could be used for email validation when entering something in an email format. 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Boundaries](#boundaries)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors
Expressions in Regex are defined between two forward slashes, such as: /abc/ - this would match any a followed by b, followed by c with no space between

At the beginning of the regex is the ^ which is used here as a Meta Escape. It's function is to define the beginning of the string we want to match.

At the end of the regex, you will notice a $. This is a special character used to define the end of the string we want to match. It also is a Meta Escape.

/^abc$/ would match only a string of "abc".

### Quantifiers
Quantifies can specify how many times the pattern is matched. In the matching email regex, there are a few different quantifiers being used. The first that occurs is the plus (+) quantifier. This matches the pattern that precedes it one or more times. Then there is the curly bracket ({}) quantifier that can set limits for a match. The curly bracket quantifier in the matching email regex can be found at near the end of the expression as seen below. The {2,6} means that the preceding string is matched a minimun of 2 times and a maximum of 6 times.

```/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/```

### Character Classes
A character class defines a set of characteristics. One example (\d) is used in the matching email regex. This character class matches any Arabic mumeral digit and is equivalent to the bracket expression [0-9]. You can this being used in the matching email regex below in the second bracket expression.

```/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/```
### Flags
The following flag being used in this example is 'g', which stands for global search.
### Grouping and Capturing
Grouping and capturing use parentheses (()) to group different parts of the string together to check and make sure they are fulfilling the requirements set for them. You can see the way the matching email regex is broken into three grouping constructs below. For the code snippet, it can contain letters a-z, numbers 0-9, an underscore, hyphen, or period. The period is an escaped character, so it required the backslash in order to be able to be matched.

```([a-z0-9_\.-]+)```

```([\da-z\.-]+)```

```([a-z\.]{2,6})```
### Bracket Expressions
Bracket expressions can be used to match characters. Anything inside of the set of square brackets ([]) will represent the chararcters that are being matched. In the matching email regex, there are three different bracket expressions as you can see below.

```[a-z0-9_\.-]```

```[\da-z\.-]```

```[a-z\.]```

### Boundaries
/b is an anchor like ^ and $. It matches at a postion that is called "word boundary". This match is zero-length.

### Look-ahead and Look-behind
Look-ahead and look-behind, collectively called “lookaround”, are zero-length assertions just like the start and end of line, and start and end of word anchors explained earlier in this tutorial. The difference is that lookaround actually matches characters, but then gives up the match, returning only the result: match or no match. That is why they are called “assertions”. They do not consume characters in the string, but only assert whether a match is possible or not. Lookaround allows you to create regular expressions that are impossible to create without them, or that would get very longwinded without them. Essentially, look-ahead allows to add a condition for “what follows”. Look-behind is similar, but it looks behind. That is, it allows to match a pattern only if there's something before it.
## Author

https://github.com/ethanquinlan1997/Regex-Tutorial