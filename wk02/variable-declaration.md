# Variable Declaration

## var

Declares a variable, optionally initializing it to a value. var declarations are globally scoped or function/locally scoped.

It is globally scoped when a var variable is declared outside a function. This means that any variable that is declared with var outside a function block is available for use in the whole window.

var is function scoped when it is declared within a function. This means that it is available and can be accessed only within that function.

**var** variables can be re-declared and updated.

```javascript
var var_name = "Hello world";
```

## let

**let** is block scoped. A block is chunk of code bounded by curly braces `{}`. Anything within curly braces is a block. So a variable declared in a block with the let is only available for use within that block.

**let** can be updated but not re-declared

```javascript
let var_name = "Hello world";
```

## const

**const** declarations are block scoped but cannot be updated or re-declared

```javascript
const pi = "3.14159";
// 3.14159
```

### Sources

[Var, let and const- what's the difference?](https://dev.to/sarah_chima/var-let-and-const--whats-the-difference-69e) by Sarah Chima

[JavaScript ES6+: var, let, or const?](https://medium.com/javascript-scene/javascript-es6-var-let-or-const-ba58b8dcde75) by Eric Elliott

#### Video

[var vs let vs const: Variable declarations in ES6 | ES2015](https://www.youtube.com/watch?v=6vBYfLCE9-Q&feature=emb_title) by Tyler McGinnis

[var, let and const - What, why and how - ES6 JavaScript Features](https://www.youtube.com/watch?v=sjyJBL5fkp8) by Fun Fun Function
