# Basic JavaScript
## Comments
```javascript
// This is an in-line comment.

/* This is a
   multi-line comment */
```
## Data types

* undefined
* null
* boolean
* string (literal)
* symbol
* number
* object

## Variables
### declaration
```javascript
var myName;
```
We tell JavaScript to create or declare a variable by putting the keyword var in front of it. It is declared with an initial value of **undefined**

### initialize when declaring
```javascript
var myVar = 5;
var myNum;
myNum = myVar;
```
In JavaScript, you can store a value in a variable with the `assignment` operator `=`. You can do it at the time of declaration, or later.

### naming convention
Variable names can be made up of:

* numbers
* letters
* $
* _

but may not contain:

* `spaces`
* start with a `number`.

```javascript
var twoWords;
var moreThanTwoWords;
var useNumbers3;
```

if the name is made of more than one word, the convention is to use so-called

* caseSensitive `cameCase` standard

## Math
```javascript
myVar = 5 + 10; // assigned 15
myVar = 12 - 6; // assigned 6
myVar = 13 * 13; // assigned 169
myVar = 16 / 2; // assigned 8
```
It is very simple to use basic math in JavaScript.

### change numbers by one
```javascript
i = i + 1;
i++;

i = i - 1;
i--;
```
It is very common to increment or decrement numbers by one, thus there is a short version to do so when needed.

### floating points
```javascript
var numDecimal = 5.6;
```
Decimal numbers are sometimes referred to as floating point numbers or floats.

### floating points calculations

In JavaScript, you can also perform calculations with decimal numbers, just like whole numbers.

### remainder
```javascript
5 % 2 = 1 because
Math.floor(5 / 2) = 2 (Quotient)
2 * 2 = 4
5 - 4 = 1 (Remainder)
+++++++++++++++++++++
17 % 2 = 1 (17 is Odd)
48 % 2 = 0 (48 is Even)
```
In mathematics, a number can be checked even or odd by checking the remainder of the division of the number by 2.

The remainder operator is sometimes incorrectly referred to as the `modulus` operator. It is very similar to modulus, but does not work properly with negative numbers.

### mathematical shortcuts
```javascript
myVar += 5;
myVar -= 5;
myVar *= 5;
myVar /= 5;
```

* augmented addition
* substraction
* multiplication
* division


## Strings
### Escaping Literal Quotes in Strings
> Escaping Literal Quotes in Strings

```javascript
var sampleStr = "Alan said, \"Peter is learning JavaScript\".";
var sampleStr = "Alan said, 'Peter is learning JavaScript'.";
var sampleStr = 'Alan said, "Peter is learning JavaScript".';
```

When you are defining a string you must start and end with a single or double quote. What happens when you need a literal quote: " or ' inside of your string?

In JavaScript, you can escape a quote from considering it as an end of string quote by placing a backslash `(\)` in front of the quote.




### Escape Sequences in Strings
>Escape Sequences in Strings

```javascript
Code	Output
\		single quote TODO
\		double quote TODO
\\		backslash
\n		newline
\r		carriage return
\t		tab
\b		backspace
\f		form feed
```
Quotes are not the only characters that can be escaped inside a string. Here is a table of common escape sequences:

### Concatenating Strings
>Concatenating Strings

```javascript
var ourStr = "Hello, our name is " + "Sylwia.";
ourStr += "I come second.";
var ourStr = "Hello, our name is " + ourName + ", how are you?";
ourStr += anAdjective;
```

* plus operator
* plus equals operator
* with variables
* with variables and plus equals operator

### String length
> String length

```javascript
var firstNameLength = 0;
var firstName = "Ada";

firstNameLength = firstName.length;
```
String Object comes with a property `.length` that gives you the ability to check the length of a given string.

### zero-based indexing
> zero-based indexing

```javascript
var firstName = "Charles";
firstName[0]; // "C"
firstName[firstName.length - 1]; // "s"
firstName[firstName.length - 3]; // "l"
```
To access string character one can use so-called **bracket notation**.

Bracket notation for last character uses string's length. So does accessing any other character from the end.

What is important is the Computer Programmers start counting from ZERO.

And because **Strings in JavaScript are immutable** the character inside a string cannot be changed!

## Arrays
```javascript
var sandwich = ["peanut butter", "jelly", "bread"].
```

Arrays are created using brackets and are **mutable**.

### Array nesting
>Array nesting

```javascript
var ourArray = [["the universe", 42], ["everything", 101010]];
```
Arrays can contain any data structure, also other arrays. This is called a **Multi-Dimensional Array**

### zero-based indexing
> zero-based indexing

```javascript
var array = [1,2,3];
array[0]; // 1
var data = array[1];  // 2
array[3] = 7; // [1, 2, 3, 7]
```

Same as strings, arrays can be accessed with bracket notation, and are zero-based. Unlike strings, arrays are mutable and elements of an array can be changed after declaration.

### multi-dimensional access
> multi-dimensional access

```javascript
var arr = [
    [1,2,3],
    [4,5,6],
    [7,8,9],
    [[10,11,12], 13, 14]
];
arr[3]; // equals [[10,11,12], 13, 14]
arr[3][0]; // equals [10,11,12]
arr[3][0][1]; // equals 11
```

Bracket notation can be used to access any array, even if the array is inside another array.

### Array manipulation methods
Array Object comes with a lot of built-in methods that can be used to manipulate and access data inside the array. Here are a few of them:

1. `.push()` - takes one or more parameters and "pushes" them onto the end of the array.
2. `.pop()` - is used to "pop" a value off of the end of an array. We can store this "popped off" value by assigning it to a variable.
3. `.shift()` -  it works just like .pop(), except it removes the first element instead of the last.
4. `.unshift()` - works exactly like .push(), but instead of adding the element at the end of the array, unshift() adds the element at the beginning of the array.

Links to documentation at Mozilla Developer Network (MDN) to commonly used methods:

* [Array/reverse](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reverse)
* [Array/join](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join)
* [Array/push](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/push)
* [Array/slice](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice)
* [Array/splice](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice)
* [Array/filter](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)
* [Array/sort](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort)
* [Array/forEach](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)
* [Array/concat](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/concat)
* [Array/pop](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/pop)

### Accessing Nested Arrays
```
var ourPets = [
  {
    animalType: "cat",
    names: [
      "Meowzer",
      "Fluffy",
      "Kit-Cat"
    ]
  },
  {
    animalType: "dog",
    names: [
      "Spot",
      "Bowser",
      "Frankie"
    ]
  }
];
ourPets[0].names[1]; // "Fluffy"
ourPets[1].names[0]; // "Spot"
```
