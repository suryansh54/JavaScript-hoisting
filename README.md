# JavaScript Hoisting

- Hoisting is JavaScript's default behavior of moving declarations to the top.
- JavaScript Declarations are Hoisted
- In JavaScript, a variable can be declared after it has been used.
- In other words; a variable can be used before it has been declared.
- Variables and constants declared with let or const are not hoisted!

```javascript
catName("Chloe");

function catName(name) {
  console.log("My cat's name is " + name);
}
/*
The result of the code above is: "My cat's name is Chloe"
*/
```

**Only declarations are hoisted**

```javascript
console.log(num); // Returns undefined 
var num;
num = 6;

// Only declarations are hoisted
num = 6;
console.log(num); // returns 6
var num;
```

```javascript
//Example 1 - Does not hoist
var x = 1; // Initialize x
console.log(x + " " + y); // '1 undefined'
var y = 2; // Initialize y
//This will not work as JavaScript only hoists declarations

//Example 2 - Hoists
var num1 = 3; //Declare and initialize num1
num2 = 4; //Initialize num2
console.log(num1 + " " + num2); //'3 4'
var num2; //Declare num2 for hoisting

//Example 3 - Hoists
a = 'Cran'; //Initialize a
b = 'berry'; //Initialize b
console.log(a + "" + b); // 'Cranberry'
var a, b; //Declare both a & b for hoisting
```
