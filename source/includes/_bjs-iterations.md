## Iterations with JavaScript _For Loops_
```javascript
for ([initialization]; [condition]; [final-expression])
```
1. initialization is evaluated on condition start
2. condition is evaluated at the start of every loop and make it run as long as it is true
3. final condition is checked at the end of the loop, usually to change the value that will change the loop, e.g. i++
```javascript
var ourArray = [];
for (var i = 0; i < 5; i++) {
  ourArray.push(i);
}

// ourArray will now contain [0,1,2,3,4]

final-expression:
i++
i += 2
i--
i -=3
etc...
```

### Loop backwards
```javascript
var ourArray = [];
for (var i=10; i > 0; i-=2) {
  ourArray.push(i);
}
```

### Loop over an array
```javascript
var ourArr = [ 9, 10, 11, 12];
var ourTotal = 0;

for (var i = 0; i < ourArr.length; i++) {
  ourTotal += ourArr[i];
}
```

### Nesting for loops
```javascript
var arr = [
  [1,2], [3,4], [5,6]
];
for (var i=0; i < arr.length; i++) {
  for (var j=0; j < arr[i].length; j++) {
    console.log(arr[i][j]);
  }
}
```

## While Loops
Another type of JavaScript loop is called a "while loop", because it runs "while" a specified condition is true and stops once that condition is no longer true.

```javascript
var ourArray = [];
var i = 0;
while(i < 5) {
  ourArray.push(i);
  i++;
}
```
