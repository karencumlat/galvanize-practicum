# Functional Programming

**Functional programming** (often abbreviated FP) is the process of building software by composing pure functions, avoiding shared state, mutable data, and side-effects. Functional programming is declarative, and application state flows through pure functions. Functional programming is a programming paradigm, meaning that it is a way of thinking about software construction based on some fundamental, defining principles (previously listed).

## Higher Order Function

A **higher order function** is a function that takes a function as an argument, or returns a function.

### filter

```javascript
let produce = [
  { type: "fruit", name: "pineapple", color: "yellow" },
  { type: "veggie", name: "carrot", color: "orange" },
  { type: "fruit", name: "strawberry", color: "red" },
  { type: "veggie", name: "broccoli", color: "green" },
];

let isFruit = function (fruit) {
  return fruit.type === "fruit";
};

const fruit = produce.filter(isFruit);

//  {type:"fruit", name:"pineapple", color:"yellow"}
//  {type:"fruit", name:"strawberry", color:"red"}
```

### map

```javascript
let name = produce.map((produce) => produce.name);

//  ["pineapple", "carrot", "strawberry", "broccoli"]
```

### reduce

```javascript
var produce = [
  { price: 3.99 },
  { price: 4.99 },
  { price: 5.99 },
  { price: 2.99 },
];

let totalPrice = produce.reduce((sum, produce) => sum + produce.price, 0);

//  17.96
```

## Destructuring

The **destructuring** assignment syntax is a JavaScript expression that makes it possible to unpack values from arrays, or properties from objects, into distinct variables.

### Array Destructuring

```javascript
let a, b, rest;

[a, b, ...rest] = [10, 20, 30, 40, 50];

console.log(rest);
// [30,40,50]
```

### Object Destructuring

```javascript
let produce = { type: "fruit", name: "apple", color: "red" };

const { type, name, color } = produce;
console.log(type);
// fruit

const { type: a, name: b, color: c } = produce;
console.log(name);
// apple
```

### Rest Parameter

The **rest** parameter syntax allows us to represent an indefinite number of arguments as an array.

```javascript
function func_name(...parameters) {
  // ... is the rest parameter
  // code to run
}
```

### Spread Operator

**Spread** or `...` syntax allows an iterable such as an array expression or string to be expanded in places where zero or more arguments (for function calls) or elements (for array literals) are expected, or an object expression to be expanded in places where zero or more key-value pairs (for object literals) are expected.

```javascript
let var_name = [...value];
```

## Closure

A **closure** is the combination of a function bundled together (enclosed) with references to its surrounding state (the lexical environment). A closure gives you access to an outer function’s scope from an inner function. In JavaScript, closures are created every time a function is created, at function creation time.

To use a closure, define a function inside another function and expose it. To expose a function, return it or pass it to another function.

The inner function will have access to the variables in the outer function scope, even after the outer function has returned.

```javascript
function grocery() {
  let item = "toilet paper";

  function groceryItem() {
    console.log("I need to buy " + item);
  }
  return groceryItem;
}

var grocery = grocery();
grocery();

// I need to buy toilet paper
```

## Currying

A **curried function** is a function that takes multiple arguments one at a time.

```javascript
let grocery = (dept) => (name) => (quantity) =>
  "I need to buy " + quantity + " " + name + " from the " + dept;

let item = grocery("produce")("apples")(3);
console.log(item);
```

## Recursion

**Recursion** is a function that calls itself until a specified condition is met.

```javascript
let countDownFrom = (num) => {
  if (num === 0) return;
  console.log(num);
  countDownFrom(num - 1);
};

countDownFrom(3);

// 3
// 2
// 1
```

## Promises

The `Promise` object represents the eventual completion (or failure) of an asynchronous operation, and its resulting value.

```javascript
let p = new Promise((resolve, reject) => {
  let sum = 2 + 2;
  if (sum === 4) {
    resolve("Correct");
  } else {
    reject("Wrong");
  }
});

p.then((msg) => {
  console.log("This is " + msg);
}).catch((error) => {
  console.log("This is " + error);
});
```

The `then` method returns a Promise. It takes up two arguments: callback functions for the success and failure cases of the Promise.

## Functor

A **Functor** is something that is Mappable or something that can be mapped between objects in a Category.

### Sources

[MDN JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

[Composing Software: The Book](https://medium.com/javascript-scene/composing-software-the-book-f31c77fc3ddc)

[Learning Functional Programming with JavaScript - Anjana Vakil - JSUnconf](https://www.youtube.com/watch?v=e-5obm1G_FY&t=1075s)

[Higher-order functions - Part 1 of Functional Programming in JavaScript](https://www.youtube.com/watch?v=BMUiFMZr7vk&list=PL0zVEGEvSaeEd9hlmCXrk5yUyqUag-n84)

[A Dead Simple intro to Destructuring JavaScript Objects](https://wesbos.com/destructuring-objects/)

[JavaScript Promises in 10 Minutes](https://www.youtube.com/watch?v=DHvZLI7Db8E)
