# Regex Tutorial

Today, we will be learning and understanding the fundumentals of Regex also, known as regular expressions. Regex is used best for any complex searches a user may want to find instead of the basic command/control + F. For my example I want to be able to understand this Regex code ```/^#?([a-f0-9]{6}|[a-f0-9]{3})$/``` which should be a hex color code.

## Summary

By the end of this tutorial the user will understand and learn how a Regex can be used to understand this code ```/^#?([a-f0-9]{6}|[a-f0-9]{3})$/```. 

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
There's mainly two different type of anchors such as ```^``` (carrot) or ```$``` (dollar). ```^``` can be used to identify the beginning word of each line while ```$``` can be used to identify the ending word of each line.

In the hex code ```/^#?([a-f0-9]{6}|[a-f0-9]{3})$/```, you can see theres an ```^``` in the second character of code, this means that it's the beginning of the line. While on the 30th character you'll see a ```$``` that means it's the end of each line.

### Quantifiers
Quantifiers are symbols that set limits to strings. Usually including the minimum and maximum. 

```*``` = 0 or more <br />
```+``` = 1 or more <br />
```?``` = 0 or 1 <br />
```{ min , max }``` = minimum, maximum  <br />
```{ n }``` = single number <br />

So for our hex code ```/^#?([a-f0-9]{6}|[a-f0-9]{3})$/``` you can see theres two different type of curly braces with a number ```{6}``` and ```{3}``` so the first hex code is 6 charactors long and the 2nd is 3 characters long. That means in this regex the code MUST be 6 digits or 3 digits long.

### OR Operator
If you want to find mulitple different type of characters you may use the OR operator to simulate that in regex codes.

```|``` = OR operator

For ```/^#?([a-f0-9]{6}|[a-f0-9]{3})$/``` you can see theres an OR operator in the middle of the hex code regex that tells us that the regex is looking for a code thats 6 strings long **OR** 3 string long.

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
