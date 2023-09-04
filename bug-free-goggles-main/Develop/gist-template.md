# REGEX email tutorial

A regular expression is a sequence of characters that specifies a matching pattern in text. In this tutorial we'll see how to use REGEX to match an email.


## Summary
In this tutorial we will see how the following Regex is used to match an email address:

var emailRegex = /\b([a-z])([\w\.]+)([^\W_]+)@([\da-z\.-]+)\.([a-z\.]{1,3})\b/g;

Below is a list of components and how they work.

## Table of Contents


- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)


## Regex Components

var emailRegex = /\b([a-z])([\w\.]+)([^\W_]+)@([\da-z\.-]+)\.([a-z\.]{1,3})\b/g;


### Quantifiers + {}

+ Matches a string that has specified characters on the left side, followed by one or more items on the right side.

e.g.:

([\w\.]+) => [\w\.] Matches any word character equivalent to \w = [a-zA-Z0-9_] or \. matches the character "." one or more times.



{} Sets an exact amount or min and max.

e.g:

([a-z\.]{1,3}) matches the previous token ([a-z\.]) between 1 and 3 times, as many times as possible.


### OR Operator [] [^...]

[] Matches a character that is within the brackets.

e.g:

[a-z] Matches the range of lower case letters from "a" to "z".



[^...] Matches a character that is not within the brackets.

e.g:

[^\W_] Matches any character that is not in the list. \W Matches any non-word character ([^a-zA-Z0-9_]) and _ matches the character "_".


### Character Classes \d \w

\d Matches a single character that is a digit.

\w Matches a word character, i.e. [a-zA-Z0-9_].


### Flags g

When writing Regex the search parameters are delimeted by two slash characters /.../ , after the second slash character is where we specify theflags.

g (global) allows for the search to continue until no more matches can be found.



### Grouping and Capturing  ()

() Captures everything inside the parenthesis. It isolates part of the match and assigns it an ID referred to later within the regex.


### Boundaries \b
A word boundary is a position between \w and \W (non-word char), or at the beginning or end of a string if it begins or ends with a word character ([0-9A-Za-z_]).

## Author

Scoges - New to programming but not to learning. <a href= "https://scoges.github.io/Portfolio/">portfolio</a>
