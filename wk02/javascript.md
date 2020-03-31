# JavaScript

**JavaScript** is a scripting language that enables you to create dynamically updating content, control multimedia, animate images, and pretty much everything else.

## Application Programming Interfaces (APIs)

APIs are ready-made sets of code building blocks that allow a developer to implement programs that would otherwise be hard or impossible to implement.

![API Categories](https://mdn.mozillademos.org/files/13508/browser.png)

* **Browser APIs** are built into your web browser, and are able to expose data from the surrounding computer environment, or do useful complex things.
  * The **DOM (Document Object Model) API** allows you to manipulate HTML and CSS, creating, removing and changing HTML, dynamically applying new styles to your page, etc.
  * The **Geolocation API** retrieves geographical information. This is how Google Maps is able to find your location and plot it on a map.
  * The **Canvas and WebGL APIs** allow you to create animated 2D and 3D graphics.
  * **Audio and Video APIs** like HTMLMediaElement and WebRTC allow you to do really interesting things with multimedia, such as play audio and video right in a web page, or grab video from your web camera and display it on someone else's computer.

* **Third party APIs** are not built into the browser by default, and you generally have to grab their code and information from somewhere on the Web.
  * The **Twitter API** allows you to do things like displaying your latest tweets on your website.
  * The **Google Maps API** and **OpenStreetMap API** allows you to embed custom maps into your website.

### Interpreted versus compiled code

* **Interpreted languages**, the code is run from *top to bottom* and the result of running the code is immediately returned.
* **Compiled languages** on the other hand are transformed (compiled) into another form before they are run by the computer. Compiled into assembly language that is then run by the computer.

### Server-side versus client-side code

* **Client-side code** is code that is run on the user's computer — when a web page is viewed, the page's client-side code is downloaded, then run and displayed by the browser.
* **Server-side code** is run on the server, then its results are downloaded and displayed in the browser.

### Dynamic versus static code

* **Dynamic code** refers to the ability to update the display of a web page/app to show different things in different circumstances, generating new content as required.
* **Static code** shows the same content all the time.

### How do you add JavaScript to your page

* Internal JavaScript - add the following in your head — just before your closing `<head>`</head> tag

```javascript
<script>
  // JavaScript goes here
</script>
```

* External JavaScript

```javascript
<script src="script.js" defer></script>
```

>**defer** attribute, tells the browser to continue downloading the HTML content once the `<script>` tag element has been reached.

```javascript
<script async src="script.js"></script>
```

>**async** attribute will download the script without blocking rendering the page and will execute it as soon as the script finishes downloading.

* Inline JavaScript handlers - sometimes you'll come across bits of actual JavaScript code living inside HTML. It might look something like this:

```javascript
function createParagraph() {
  let para = document.createElement('p');
  para.textContent = 'You clicked the button!';
  document.body.appendChild(para);
}

<button onclick="createParagraph()">Click me!</button>
```

### Comments

```javascript
// I am a single line comment

/*
  I am a
  multi-line
  a comment
*/
```

### Variable

* Declaration - introduces a new identifier

```javascript
var var_name;
```

* Initialization - assign a value to a variable

```javascript
var_name = "This is an assigned value";
```

* Scope - defines where a variables and functions are accessible inside a program
  * Global scope - variable created as members of the global object
  * Function scope - variable occurs inside a function declaration

### var vs let vs const

* var - function scope
* let - block scope {}
* const - once a value is assigned, cannot reassign new value

## Videos

[Brandon Eich - A Brief History of JavaScript](https://www.youtube.com/watch?v=aX3ZABCdC38)

[The Weird History of JavaScript](https://www.youtube.com/watch?v=Sh6lK57Cuk4)

[var, let and const - What, why and how - ES6 JavaScript Features](https://www.youtube.com/watch?v=sjyJBL5fkp8) by Fun Fun Function

## Articles

[Javascript](https://developer.mozilla.org/en-US/docs/Web/JavaScript) by MDN web docs

[JavaScript: The World's Most Misunderstood Programming Language](https://www.crockford.com/javascript/javascript.html) by Douglas Crockford
