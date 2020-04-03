# Array Method

## Converting between strings and arrays

The **join** method creates and returns a new string by concatenating all of the elements in an array (or an array-like object), separated by commas or a specified separator string. If the array has only one item, then that item will be returned without using the separator.

```javascript
let num = "one, two, three";

let num_arr = num.split(",");
num_arr; // ['one','two','three]

let num_str = num_arr.join(",");
num_str; //'one, two, three'

let fruit_arr = ["Pineapple", "Cantaloupe", "Honeydew"];
fruit_arr.toString(); //'Pineapple, Cantaloupe, Honeydew'
```

## Adding and removing array items

The **push** method adds one or more elements to the end of an array and returns the new length of the array.

```javascript
fruit_arr.push("Strawberry");
fruit_arr; // ["Pineapple", "Cantaloupe", "Honeydew", "Strawberry"]
```

The **pop** method removes the last element from an array and returns that element. This method changes the length of the array.

```javascript
fruit_arr.pop();
// ["Pineapple", "Cantaloupe", "Honeydew"]
```

The **unshift** method adds one or more elements to the beginning of an array and returns the new length of the array.

```javascript
fruit_arr.unshift("Strawberry");
// ["Strawberry", "Pineapple", "Cantaloupe", "Honeydew"]
```

The **shift** method removes the first element from an array and returns that removed element. This method changes the length of the array.

```javascript
fruit_arr.shift();
// ["Pineapple", "Cantaloupe", "Honeydew"]
```

## Array Iteration

The **forEach** method executes a provided function once for each array element.

```javascript
let fruit_arr = ["Pineapple", "Cantaloupe", "Honeydew"];

fruit_arr.forEach(function(item, index, array) {
  console.log(item, index);
});

//Pineapple 0
//Cantaloupe 1
//Honeydew 2
```

Sorts the elements of an array in place and returns the array.

```javascript
let fruit_arr = ["Pineapple", "Cantaloupe", "Honeydew"];

console.log(fruit_arr.sort());

//Cantaloupe
//Honeydew
//Pineapple
```

## Videos

[Arrays - Beau teaches JavaScript](https://www.youtube.com/watch?v=QEZXbRiaY1I&list=PLWKjhJtqVAbk2qRZtWSzCIN38JC_NdhW5&index=16&t=0s)

[Common Array Methods - Beau teaches JavaScript](https://www.youtube.com/watch?v=MeZVVxLn26E&list=PLWKjhJtqVAbk2qRZtWSzCIN38JC_NdhW5&index=17&t=1s)

[Array Iteration: 8 Methods - map, filter, reduce, some, every, find, findIndex, forEach](https://www.youtube.com/watch?v=Urwzk6ILvPQ&list=PLWKjhJtqVAbk2qRZtWSzCIN38JC_NdhW5&index=23&t=0s)
