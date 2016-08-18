## Number generation
### Fraction, from 0 to 1, exclusive.
```javascript
var number = Math.random();
```
### Random Whole Numbers
```javascript
var num = Math.floor(Math.random() * 10);
```
1. Use Math.random() to generate a random decimal.
2. Multiply that random decimal by 10.
3. Use another function, Math.floor() to round the number down to its nearest whole number
4. It gives from 0 to 9 inclusive

### Generate numbers within a Range (min to max inclusive)
```javascript
var number Math.floor(Math.random() * (max - min + 1)) + min
```
## Regular expressions
Regular expressions are used to find certain words or patterns inside of strings. For example, if we wanted to find the word the in the string The dog chased the cat, we could use the following regular expression: /the/gi

Let's break this down a bit:

1. `/` is the start of the regular expression.
2. `the` is the pattern we want to match.
3. `/` is the end of the regular expression.
4. `g` means global, which causes the pattern to return all matches in the string, not just the first one.
5. `i` means that we want to ignore the case (uppercase or lowercase) when searching for the pattern.
6.  `\s` to find whitespace in a string.
7.  `\d` to find digits
8.  You can invert any match by using the uppercase version of the regular expression selector. For example, `\s` will match any whitespace, and `\S` will match anything that isn't whitespace.

```javascript
var testString = "There are 3 cats but 4 dogs.";
var expression = /\d+/g;
var digitCount = testString.match(expression).length;
// 2
var digitCount = testString.match(expression).;
// ["3","4"]
```

### Whitespace characters
```javascript
" " (space)
\r (the carriage return)
\n (newline)
\t (tab)
\f (the form feed)

var spaceCount = testString.match(expression).length;
// 6
```

FIND MORE INFO ABOUT

1. If you do a mathematical operation on an undefined variable your result will be NaN which means "Not a Number". If you concatenate a string with an undefined variable, you will get a literal string of "undefined".
4
