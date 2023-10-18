# Regex but in simple english

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ 

If you have no idea what you are looking at, dont worry. I've been there. That is a Regex expression. I will explain what it is, how it works, and how one could use it. 

## Summary

Regex is kind of like using command F to search for what one is looking for. Basiaclly a regex is like a complicated version of that. So the regex that you saw earlier "  /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/  " is used to search for email. if you look closely you can see "a-z" which is characters a through z. You can also see "0-9" for the digits 0 through 9. there is an _\.- and those are characters you could put in a email. you can see the @ sign is outside of the parenthesis and I will explain that down below but this was just a simple intro. 

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
The regex needs to be wrapped between two "/"
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ 
As you can see above it is wrapped. 
### Anchors
So for the anchors we got two. There is the "^" and the "$" 
^ means that a string begins with the next character. 
For example ^Would  will return matches such as "Would you still want to go." 
It will not return " I would not like to go " The reason it wont is because regex is case sensetive.  
### Quantifiers
So at the end of the example you can see {2,6}
Usually this means that froma all of matches is will only return the string with at least 2 characters and no more than 6 characters.
{ 5 } will bring up exactly 5 characters
{ 5, } will bring up at least 5 characters
{ 5,9 } will bring up minimum of 5 and no more than 9 characters


### OR Operator
There is an Or operator which is |
an example would be (1|2|3):(4|5|6)
this would return 2:4 12:6 123:4 123:45 and 123:456. 

### Character Classes
. would match any character except the newline character
\d would match any arabic numeral digit. Its the same as writing [0-9]
\w would match any alphanumeric number its the same as [A_Za-z0-9]
\s would match a whitespace character
### Flags
g is a global search. the regex would be tested against all psoibilities
i is for case insensitive. Basically its not case sensitive like it normally is
m is for multi line search It treats a multi line input as multiple lines.

### Grouping and Capturing
Grouping is quite simple, Its just grouped by parenthesis. 
in the example we have ([a-z0-9_\.-]+)    @     ([\da-z\.-]+)
I seperated them with spaces for readibility. Once its seperated you can see whats going on inside the group. 
### Bracket Expressions
So anything inside square brackets [] means that its a range. For example a-z. 
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ 
As you can see a-z is inside the square bracket so that means any character between a and z. 
If you have a square bracket with no " - " it would look for a string that has the characters that match.
For example [ab] would return "aaaaaaaabbbbbbbbb" "ab" "apple" "bannana" and "books"
It would return any string that has a matching character.
Back to the dashes. [0-9] would return a string that contains any number between 0-9.
So basically if its in between brackets it would return the matching character. 
You can also conmbine the searches so in the example above the first half we have 
[a-z0-9_\.-] this would return any matches with a-z 0-9 and the special characters _ / . -
If there is an ^ inside the bracket its kind of like an ! where its the opposite.
For example [^m] would would find any strings without the character m
### Greedy and Lazy Match
There are two types of searches. There are greedy and lazy matches. Quantifiers are greedy. 
When the search is greedy it will try to match as many occurrences as possible while if the search is lazy it will match as few as possible. The search can be made lazy by adding a " ? "
### Boundaries
There word bounderies. So "\b" is the boundary. The \b needs to be wrapped aound the word. This means that a search would return whole words only. 

### Back-references
Back references are like shortcuts. You can use the following
(\w+) captures the first word
\s matches the space
\1 will make sure that the second word is the same as the first word
### Look-ahead and Look-behind
There are 4 types for look ahead and look behind.
There is positive look ahead which is saying I want to find the sentences that comes before the keyword
There is negative look ahead which is saying I want to find the rest of the sentences that do not have the keyword behind them
There is positive look behind which is saying I want to find the sentences that come after the keyword
Finally there is negative look behind which is saying I want to find the rest of the senteces that do not have the keyword after them

Positive look ahead is ?=
negative look ahead is ?!
positive look behind is ?<=
Negative look behind is ?<
## Author

My name is Marien Castellanos. I am currently doing a coding bootcamp. If you want to check out my other projects I will leave a link right below

https://github.com/mariencito