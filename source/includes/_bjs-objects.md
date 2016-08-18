## JavaScript Objects
Objects are similar to arrays, except that instead of using indexes to access and modify their data, you access the data in objects through what are called **properties**.

```javascript
var cat = {
  "name": "Whiskers",
  "legs": 4,
  "tails": 1,
  "enemies": ["Water", "Dogs"]
};
```

### Accessing Objects Properties
1. Dot Operator
2. Bracket Notation - If the property of the object you are trying to access has a space in it, you will need to use bracket notation
3. Variables

> .DOT Operator

```javascript
var myObj = {
  prop1: "val1",
  prop2: "val2"
};
var prop1val = myObj.prop1; // val1
var prop2val = myObj.prop2; // val2
```

> [ ] BRACKET

```javascript
var myObj = {
  "Space Name": "Kirk",
  "More Space": "Spock"
};
myObj["Space Name"]; // Kirk
myObj['More Space']; // Spock
```

> Variables

```javascript
var someProp = "propName";
var myObj = {
  propName: "Some Value"
}
myObj[someProp]; // "Some Value"
```

> Updating properties

```javascript
var ourDog = {
  "name": "Camper",
  "legs": 4,
  "tails": 1,
  "friends": ["everything!"]
};

ourDog.name = "bow-wow";
```

> Adding properties

```javascript
var ourDog = {
  "name": "Camper",
  "legs": 4,
  "tails": 1,
  "friends": ["everything!"]
};

ourDog.bark = "bow-wow";
```

> Deleting properties

```javascript
delete ourDog.bark;
```

###  Using object as lookup/library/storage
> Using object as lookup/library/storage

```javascript
var alpha = {
  1:"Z",
  2:"Y",
  3:"X",
  4:"W",
  ...
  24:"C",
  25:"B",
  26:"A"
};
alpha[2]; // "Y"
alpha[24]; // "C"

var value = 2;
alpha[value]; // "Y"
```

### Accessing Nested Objects
The sub-properties of objects can be accessed by chaining together the dot or bracket notation.

> Accessing Nested Objects

```javascript
var ourStorage = {
  "desk": {
    "drawer": "stapler"
  },
  "cabinet": {
    "top drawer": {
      "folder1": "a file",
      "folder2": "secrets"
    },
    "bottom drawer": "soda"
  }
};
ourStorage.cabinet["top drawer"].folder2;  // "secrets"
ourStorage.desk.drawer; // "stapler"
```

### Object methods
`.hasOwnProperty(propname) // returns true or false`

## JSON
### Complex data structure JSON = JavaScript ObjectNotation
```javascript
var ourMusic = [
  {
    "artist": "Daft Punk",
    "title": "Homework",
    "release_year": 1997,
    "formats": [
      "CD",
      "Cassette",
      "LP" ],
    "gold": true
  }
];
```
Objects hold data in a property, which has a key-value format. In the example above, "artist": "Daft Punk" is a property that has a key of "artist" and a value of "Daft Punk".
