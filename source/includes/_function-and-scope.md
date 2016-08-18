
## Functions
### Function declaration
>Function declaration

```
function functionName() {
  console.log("Hello World");
}
```

### Function invoked
>Function invoked

```
functionName();
```

### Passing Values to Functions with Arguments
>Passing Values to Functions with Arguments

```
function testFun(param1, param2) {
  console.log(param1, param2);
}

testFun("Hello", "World");
```
**Parameters** are variables that act as placeholders for the values that are to be input to a function when it is called.

When a function is defined, it is typically defined along with one or more parameters. The actual values that are input (or "passed") into a function when it is called are known as **arguments**.

## Scope
> Scope

```
function myTest() {
  var loc = "foo";
  console.log(loc);
}
myTest(); // "foo"
console.log(loc); // "undefined"
```

### Global Scope
In JavaScript, scope refers to the **visibility of variables**. Variables which are defined outside of a function block have **Global scope**. This means, they can be seen **everywhere** in your JavaScript code.

### Local Scope
Variables which are declared within a function, as well as the function parameters have local scope. That means, they are only visible within that function.

**Declaring a variable inside a function without `var` will create it in a Global scope !!!**

It is possible to have both local and global variables with the same name. When you do this, the local variable takes precedence over the global variable. BUT DO NOT!!!

### Return a Value from a Function with Return, and assign to a variable
We can pass values into a function with arguments. You can use a return statement to send a value back out of a function.

> Return a Value from a Function

```
function plusThree(num) {
  return num + 3;
}
var answer = plusThree(5); // 8
```

## Queue
In Computer Science a queue is an abstract Data Structure where items are kept in order. New items can be added at the back of the queue and old items are taken off from the front of the queue.

## Boolean values
```
true
false
```

```
function isEqual(a,b) {
  return a === b;
}
```


## Conditional Logic with If Statements
```
if (condition is true) {
  statement is executed
}
```

```
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
```
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


```
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
