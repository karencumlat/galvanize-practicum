# Function

## Function Declaration

The **function declaration** also called function definition or function statement consists of the `function` keyword, followed by

- The name of the function
- A list of parameters to the function, enclosed in parentheses and separated by commas
- The JavaScript statements that define the function, enclosed in curly brackets `{...}`

```javascript
function func_name(parameter, param2, ...,paramN){
  //code to run
}
```

## Function Expression

A **function expression** can be stored in a variable, the variable can be use as a function. It does not require function name. It always invoked using the variable name.

```javascript
let func_var = function (parameter, param2, ..., paramN) {
   //code to run
};
```

## Arrow Function

**Arrows** are a function shorthand using the `=>` syntax. It is syntactically compact alternative to a regular function expression. They are ill suited as methods, and they cannot be used as constructors.

```javascript
(argument1, argument2, ...argumentN) => {
  // code to run
};
```
