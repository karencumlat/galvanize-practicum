# String

## Useful string methods

### Finding the length of a string

```javascript
let str = "string";
str.length;
// 6
```

### Retrieving a specific string character

```javascript
str[0];
//s
```

### Finding a substring inside a string and extracting it

```javascript
str.indexOf("ing");
//3
```

### Changing case

```javascript
let str = "My NaMe is";
str.toLowerCase();
// my name is
str.toUpperCase();
// MY NAME IS
```

### Updating parts of a string

```javascript
str.replace("string", "str");
//str
```

The **trim** method removes whitespace from both ends of a string. Whitespace in this context is all the whitespace characters (space, tab, no-break space, etc.) and all the line terminator characters (LF, CR, etc.).

```javascript
const greeting = "   Hello world!   ";

console.log(greeting);
// expected output: "   Hello world!   ";

console.log(greeting.trim());
// expected output: "Hello world!";
```

## Template Literals

**Template literals** are string literals allowing embedded expressions. You can use multi-line strings and string interpolation features with them.

- Enclosed by the backtick (``) characters instead of double or single quotes.
- Can contain placeholders, indicated by the dollar sign and curly braces (\${expression})

```javascript
let placeholder = "expression";
let temp_literal = `Sample of template literal
with ${placeholder}`;

// Sample of template literal
// with expression
```

## Videos

[20 String Methods in 7 Minutes - Beau teaches JavaScript](https://www.youtube.com/watch?v=VRz0nbax0uI&list=PLWKjhJtqVAbk2qRZtWSzCIN38JC_NdhW5&index=7&t=0s)

[Template Literals (ES6) - Beau teaches JavaScript](https://www.youtube.com/watch?v=kj8HU-_P2NU&list=PLWKjhJtqVAbljtmmeS0c-CEl2LdE-eR_F&index=5&t=0s)
