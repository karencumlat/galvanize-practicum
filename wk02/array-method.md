# Array Method

## Converting between strings and arrays

```javascript
let num = 'one, two, three';

let num_arr = num.split(',');
num_arr; // ['one','two','three]

let num_str = num_arr.join(',');
num_str; //'one, two, three'

let fruit_arr = ['Pineapple','Cantaloupe', 'Honeydew'];
fruit_arr.toString(); //'Pineapple, Cantaloupe, Honeydew'
```

## Adding and removing array items

```javascript
fruit_arr.push('Strawberry');
fruit_arr; // ["Pineapple", "Cantaloupe", "Honeydew", "Strawberry"]

fruit_arr.pop();
// ["Pineapple", "Cantaloupe", "Honeydew"]

fruit_arr.unshift('Strawberry');
// ["Strawberry", "Pineapple", "Cantaloupe", "Honeydew"]

fruit_arr.shift();
// ["Pineapple", "Cantaloupe", "Honeydew"]
```

## Videos

[Arrays - Beau teaches JavaScript](https://www.youtube.com/watch?v=QEZXbRiaY1I&list=PLWKjhJtqVAbk2qRZtWSzCIN38JC_NdhW5&index=16&t=0s)

[Common Array Methods - Beau teaches JavaScript](https://www.youtube.com/watch?v=MeZVVxLn26E&list=PLWKjhJtqVAbk2qRZtWSzCIN38JC_NdhW5&index=17&t=1s)
