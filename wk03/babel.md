# Babel

`Babel` is a JavaScript compiler

![Babel logo](https://raw.githubusercontent.com/babel/logo/master/babel.png)

`Babel` is a toolchain that is mainly used to convert ECMAScript 2015+ code into a backwards compatible version of JavaScript in current and older browsers or environments. Here are the main things Babel can do for you:

- Transform syntax
- Polyfill features that are missing in your target environment (through @babel/polyfill)
- Source code transformations (codemods)

```javascript
// Babel Input: ES2015 arrow function
[1, 2, 3].map((n) => n + 1);

// Babel Output: ES5 equivalent
[1, 2, 3].map(function (n) {
  return n + 1;
});
```

## Sources

[Babel](https://babeljs.io/)

## ES Modules

[JavaScript ES6 Modules](https://www.youtube.com/watch?v=cRHQNNcYf6s)
[JavaScript Modules: ES6 Import and Export](https://www.youtube.com/watch?v=_3oSWwapPKQ)
