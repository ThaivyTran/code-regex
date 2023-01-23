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
There's mainly two different type of **anchors** such as ```^``` (carrot) or ```$``` (dollar). ```^``` can be used to identify the beginning word of each line while ```$``` can be used to identify the ending word of each line.

In the hex code ```/^#?([a-f0-9]{6}|[a-f0-9]{3})$/```, you can see theres an ```^``` in the second character of code, this means that it's the beginning of the line. While on the 30th character you'll see a ```$``` that means it's the end of each line.

### Quantifiers
**Quantifiers** are symbols that set limits to strings. Usually including the minimum and maximum. 

```*``` = 0 or more <br />
```+``` = 1 or more <br />
```?``` = 0 or 1 <br />
```{ min , max }``` = minimum, maximum  <br />
```{ n }``` = single number <br />

So for our hex code ```/^#?([a-f0-9]{6}|[a-f0-9]{3})$/``` you can see theres two different type of curly braces with a number ```{6}``` and ```{3}``` so the first hex code is 6 charactors long and the 2nd is 3 characters long. That means in this regex the code MUST be 6 digits or 3 digits long. We also have a ```?``` quantifier which means it'll search for less strings in other words known as ***lazy***.

### OR Operator
If you want to find mulitple different type of characters you may use the **OR operator** to simulate that in regex codes.

```|``` = OR operator

For ```/^#?([a-f0-9]{6}|[a-f0-9]{3})$/``` you can see theres an OR operator in the middle of the hex code regex that tells us that the regex is looking for a code thats 6 strings long ***OR*** 3 string long.

### Character Classes
**Character classes** helps identify sets of characters in regex. Usually in square brackets.

```\d``` = digits <br />
```.``` = any character <br />
```*``` = 0 or more <br />
```.*``` = wild card <br />
```\w``` = any character (A-Z, a-z & 0,9) <br />
```\W``` = anything **without** a character <br />
```\s``` = whitespace (space or tab) <br />
```\S``` = anything **without** whitespace <br />
```\.``` = literal character <br />

In our hex code ```/^#?([a-f0-9]{6}|[a-f0-9]{3})$/``` theres two sets of square brackets. ```[a-f0-9]``` and ```[a-f0-9]```, they both are literally saying the same thing. Which means the regex is looking for codes that fit that requirement in the square brackets, so for letters the regex will look for any letters that is from ***a*** to ***f*** (a,b,c,d,e,f). Then for numbers the regex will look for numbers that is from ***0*** to ***9*** (0,1,2,3,4,5,6,7,8,9).

### Flags
**Flags** are included at the ***end*** of the regex, after the 2nd slash, it's to help specify the regex search.

```i``` = case-insensitive <br />
```g``` = all matches <br />
```m``` = multi-line search <br />
```s``` = enables ```.``` <br />

When understanding flags it's mainly used like an "advanced search" option. So if you add an ```i``` before the second slash it'll look for code that has both letter uppercase and lowercase in the word. By adding a ```g``` it'll search for all the matches the regex can find etc.

In our example hex code, ```/^#?([a-f0-9]{6}|[a-f0-9]{3})$/``` are there any flags you can see? No right? That means our code isn't limited to any search but the require letters and numbers.

### Grouping and Capturing
**Capturing groupings** can be used to group strings into subgroups by using parenthesis.<br /> 
<br /> 
For example with phone numbers the regex code will appear like this ```\d{3}-\d{3}-\d{4}```. Say you want to only get the area code of each phone number, then creating a subgroup will help search for ***only*** the area codes. The regex code should look like this, ```(\d{3})-\d{3}-\d{4}```. At the end the regex should only look for the first 3 digits of each phone number. If you ***only*** want to search for the last four digits then just add the parenthesis at the end like so, ```\d{3}-\d{3}-(\d{4})``` or if you ***only*** want the middle 3 digits then it should look like ```\d{3}-(\d{3})-\d{4}```. 

Do you see any groupings in our example hex code? ```/^#?([a-f0-9]{6}|[a-f0-9]{3})$/``` Yes, we currently are looking for a grouping of hex code at a time. So when we search in regex we should see common groupings of code thats 3-6 digits long.

### Bracket Expressions

### Greedy and Lazy Match
Greedy and lazy matches, are the complete opposites of each other. A **greedy** match will search for many patterns as possible while a **lazy** match will search for the least patterns.

Majority of quanitifers are ***greedy*** matches such as ```+``` and ```*```, while ```?``` is a ***lazy*** match.

As stated in **quantifiers** we have one ```?``` in our hex code example ```/^#?([a-f0-9]{6}|[a-f0-9]{3})$/``` so the regex will search for one pattern at a time.

### Boundaries
**Boundaries** are used to help match words you want the letter to begin with or end. You can also use it for searching words within words.

```\b``` = whole words ***only*** <br />
```\B``` = matches any position <br />

An example of this is let's say we want to search for ```cat```. We would do a regex that looks like this ```\bcat``` this regex is currently searching for any words that starts with ```cat```, so maybe ```cats``` or ```categories``` will appear. But if you want to search words that ends with ```cat``` then you would put the ```\b``` at the end like so, ```cat\b```. So maybe words like ```tacocat``` or ```tomcat``` will appear.

When using ```\B``` that means that it'll do the opposite of ```\b``` so no matter where ```cat``` is located, words like ```locate``` or ```vacate``` will appear because it includes ```cat``` inside the word.

### Back-references
**Back-references** are used in regex to search for mutiple same characters.

### Look-ahead and Look-behind

## Author
Hello! My name is Thaivy Tran and I'm new to coding! I hope you find this beginners tutorial useful! Feel free to contact me at my email, Tran.Thaivy1997@gmail.com for any suggestions on making this Regex tutorial better!
For more look at my Github profile, <a href="https://github.com/ThaivyTran">@ThaivyTran</a>.
