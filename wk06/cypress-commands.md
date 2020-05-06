# Cypress Commands

## click

Click a DOM element.

```js
cy.get(".btn").click(); // Click on button
cy.focused().click(); // Click on el with focus
cy.contains("Welcome").click();
```

## children

Get the children of each DOM element within a set of DOM elements.

## contains

Get the DOM element containing the text. DOM elements can contain more than the desired text and still match. Additionally, Cypress prefers some DOM elements over the deepest element found.

```js
cy.get(".nav").contains("About"); // Yield el in .nav containing 'About'
cy.contains("Hello"); // Yield first el in document containing 'Hello'
```

## deep.equal(value)

```js
expect(obj).to.deep.equal({ name: "Jane" });
```

## eq

Get A DOM element at a specific index in an array of elements.

> The querying behavior of this command matches exactly how .eq() works in jQuery. Its behavior is also similar to that of the CSS pseudo-class :nth-child() selector.

```js
cy.get("tbody>tr").eq(0); // Yield first 'tr' in 'tbody'
cy.get("ul>li").eq(4); // Yield fifth 'li' in 'ul'
```

## focused

Get the DOM element that is currently focused.

```js
cy.focused(); // Yields the element currently in focus
```

## get

Get one or more DOM elements by selector or alias.

```js
cy.get(".list > li"); // Yield the <li>'s in .list
```

## parent

Get the parent DOM element of a set of DOM elements.

```js
cy.get("header").parent(); // Yield parent el of `header`
```

## scrollTo

Scroll to a specific position.

```js
cy.scrollTo(position);
cy.scrollTo(x, y);
```

## should

Create an assertion. Assertions are automatically retried until they pass or time out.

```js
cy.get(".error").should("be.empty"); // Assert that '.error' is empty
cy.contains("Login").should("be.visible"); // Assert that el is visible
cy.wrap({ foo: "bar" }).its("foo").should("eq", "bar"); // Assert the 'foo' property equals 'bar'
```

## then

cy.get('header').parent() // Yield parent el of `header`

```js
cy.get(".nav").then(($nav) => {}); // Yields .nav as first arg
cy.location().then((loc) => {}); // Yields location object as first arg
```

## trigger

Trigger an event on a DOM element.

```js
cy.get("a").trigger("mousedown"); // Trigger mousedown event on link
```

## wait

Wait for a number of milliseconds or wait for an aliased resource to resolve before moving on to the next command.

```js
cy.wait(500);
```

## Source

[Cypress API](https://docs.cypress.io/api/api/table-of-contents.html)
