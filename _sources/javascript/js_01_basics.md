# Javascript basics

## Variable declaration
```js
var foo = "hello" // scoped to the function.
let foo = "hello" // scoped to the immediate enclosing block denoted by { }.
```

## Data types
### numbers
- Mathematical operations
```js
var myNb = 1 + 2;
var myNb = 1 - 2;
var myNb = 1 * 2;
var myNb = 1 / 2;
var myNb = 1 % 2; // modulo
```
- increment and decrement
```js
var myNb = 5;
myNb ++; // increment by 1
myNb --;// decrement by 1
myNb += 10; // add 10
// Also works with other operators: -= *= /=
```
### string
```js
"a" + "b" // will concatenate to: "ab"
```

### boolean
```js
var x = true;
var y = false;
```

## Comparators

|Comparator |definition |
|--         |--         |
|==         | is equal to (does not consider data type)|
|===        | is equal to (considering data type)|
|!==        | is NOT equal to|
|>          | is greater than|
|<          | is lesser than|
|>=         |is greater or equal to|
|<=         |lesser or equal to|
|||
## Combinors
|Combinor |definition |
|--       |--         |
|&&       | AND       |
|\|\      | OR          |
|!        | NOT / The opposite|
|||
## Control statements:
### If-Else
```js
if(condition === true){
  /* do something */
} else{
  turnRight();
}
```
```js
if (condition1 === true) {
  /* do something */
} else if (condition2 === true) {
  /* do something */
} else {
  /* do something */
}
```
### While
```js
while(condition === true){
  //instructions
}
```
### For loops
```js
for(startcondition; endcondition; action){
  //instructions
}
```
### Switch


## Arrays
```js
var myArray = ["a","z","e","r","t","y"];
```
- Retrieve item by position:
```js
myArray[1]; // Would return "z"
```
- Get list length:
```js
myArray.length; // Would return 6
```
- Test if item is in a list
```js
myArray.includes("t"); // Return a bool, here 'True'
```
- Adding item to the end
```js
myArray.push("u"); // myArray is updated with a 'u' at its end.
```
- Return and delete last item
```js
myArray.pop(); // Return the last item and delete it from the list.
```


## Common functions

### Browser popups related
- Open a browser popup with text
```js
alert("hello world");
window.alert("hello world");
```

- Open a browser popup with a prompt
```js
prompt("what is your name?");
```
### string related
- Count characters in a string:
```js
myVar.length; //will return a number.
```

- Get a part of a string
```js
var name = "Romain";
name.slice(0,3); // This will return 'Rom'.
```

- Change string to upper/lowercase
```js
var name = "ROMain";
name.toUpperCase(); // This will return 'ROMAIN'.
name.toLowerCase(); // This will return 'romain'.
```

### Misc
- Print in console:

```js
console.log("Hello world");
```

- Get the datatype of something:
```js
typeof(2+3);
```

 ## Functions
- Declaring a basic function:
 ```js
function getMilk(){
  // instructions
}
// Calling the function:
getMilk();
```
- Declaring a function with parameters:
 ```js
function getMilk(bottles){
  //instructions
}
// Calling the function:
getMilk(2);
```
- Declaring a function returning output:
```js
function getMilk(bottles){
  //instructions
  return
}
// Calling the function:
getMilk(2);
```

### Math functions
weight/Math.pow(height,2))
- Round number
 ```js
Math.floor(3.6); // Round down to 3

Math.round(3.3); // Return 3
Math.round(3.6); // Return 4
```
- Calculate the power of a number
 ```js
Math.pow(3,2); // Equals to 3². Return 9
```
- Get random number
 ```js
Math.random(); // return a float between 0 and 0.9999999999
```
