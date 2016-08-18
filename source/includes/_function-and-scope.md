
## Functions
### Function declaration
>Function declaration

```javascript
function functionName() {
  console.log("Hello World");
}
```

### Function invoked
>Function invoked

```javascript
functionName();
```

### Passing Values to Functions with Arguments
>Passing Values to Functions with Arguments

```javascript
function testFun(param1, param2) {
  console.log(param1, param2);
}

testFun("Hello", "World");
```
**Parameters** are variables that act as placeholders for the values that are to be input to a function when it is called.

When a function is defined, it is typically defined along with one or more parameters. The actual values that are input (or "passed") into a function when it is called are known as **arguments**.

## Scope
> Scope

```javascript
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

```javascript
function plusThree(num) {
  return num + 3;
}
var answer = plusThree(5); // 8
```
