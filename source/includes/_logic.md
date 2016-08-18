
## Queue
In Computer Science a queue is an abstract Data Structure where items are kept in order. New items can be added at the back of the queue and old items are taken off from the front of the queue.

## Boolean values
```javascript
true
false
```

```javascript
function isEqual(a,b) {
  return a === b;
}
```


## Conditional Logic with If Statements
```javascript
if (condition is true) {
  statement is executed
}
```

```javascript
function test (myCondition) {
  if (myCondition) {
     return "It was true";
  }
  return "It was false";
}
test(true);  // returns "It was true"
test(false); // returns "It was false"
```
## Early Pattern
```javascript
function myFun() {
  console.log("Hello");
  return "World";
  console.log("byebye")
}
myFun();
```
The above outputs "Hello" to the console, returns "World", but "byebye" is never output, because the function exits at the return statement.

## Comparison Operators

* equality operator `==`
* strict equality operator `===`
* Inequality Operator `!=`
* Strict Inequality Operator `!==`
* Greater Than Operator `>`
* Greater Than Or Equal To Operator `>=`
*  Less Than Operator `<`
* Less Than Or Equal To Operator `<=`
* Logical And Operator `&&`
* Logical Or Operator `||`


```javascript
1   ==  1    // true
1   ==  2    // false
1   == '1'   // true
"3"  ==  3    // true

3 === 3   // true
3 === '3' // false

1 != 2      // true
1 != "1"    // false
1 != '1'    // false
1 != true   // false
0 != false  // false

3 !== 3   // false
3 !== '3' // true
4 !== 3   // true

 5 > 3   // true
 7 > '3' // true
 2 > 3   // false
'1' > 9  // false

 6  >=  6  // true
 7  >= '3' // true
 2  >=  3  // false
'7' >=  9  // false

  2 < 5  // true
'3' < 7  // true
  5 < 5  // false
  3 < 2  // false
'8' < 4  // false

  4 <= 5  // true
'7' <= 7  // true
  5 <= 5  // true
  3 <= 2  // false
'8' <= 4  // false

++++++++++++++++++++++++++++
if (num > 5 && num < 10) {
  return "Yes";
}
return "No";
++++++++++++++++++++++++++++
if (num > 10 || num < 5) {
  return "No";
}
return "Yes";

```

## Else if and Else Statements

```javascript
if (num > 15) {
  return "Bigger than 15";
} else if (num < 5) {
  return "Smaller than 5";
} else {
  return "Between 5 and 15";
}
```
## Switch Statements
If you have many options to choose from, use a switch statement. A switch statement tests a value and can have many case statements which defines various possible values. Statements are executed from the first matched case value until a break is encountered. Case values are tested with strict equality.

```javascript
switch (val) {
  case 1:
  case 7: (can be two like this as well)
    answer = "apple";
    break;
  case 2:
    answer = "bird";
    break;
  case 3:
    answer = "cat";
    break;
  default:
	  answer = "stuff";  
}
```
