# Paprika

## Getting Started

### Clone

Clone the Paprika repository

```bash
$git clone https://github.com/acl-services/paprika.git
```

### Build

#### Install dependencies

```bash
$yarn
```

#### Link packages with Lerna

`Lerna` is a tool for managing JavaScript projects with multiple
packages.

Link local packages together and install remaining package dependencies

```bash
$npx lerna bootstrap
```

## Button Component Testing

### noop

`noop` short for **no operation** is a computer instruction that takes up a small amount of space but **specifies no operation**.

### RegExp i Modifier

`i` performs **case-insensitive matching**

```javascript
return render(
  <Button {...defaultProps} {...props}>
    {props.children || "happy button"}
  </Button>
);

fireEvent.click(getByText(/happy button/i));
```

### a11y

Accessibility or `a11y` (as in "a" then 11 characters then "y") is a measure of how accessible a computer system is to all people, including those with disabilities or impairments.

#### role attribute

#### semantic

relating to meaning in language

> For example, isSemantic: true will render a \<button> component while isSemantic: false, it will render different element such as \<span>

## Testing Library

### React Testing Library API

```javascript
import { render, fireEvent } from "@testing-library/react";
```

#### render

Render into a container which is appended to _document.body_

#### fireEvent

```javascript
fireEvent((node: HTMLElement), (event: Event));
```

### DOM Testing Library Queries

#### getByLabelText

`getByLabelText`: Only really good for form fields, but this is the number one method a user finds those elements, so it should be your top preference.

#### getByText

`getByText`: Not useful for forms, but this is the number 1 method a user finds most non-interactive elements (listitems or divs).

```javascript
getByText(/happy button/i);
```

#### querySelector (manual queries)

`querySelector(selectors)` returns the first Element within the document that matches the specified selector, or group of selectors. If no matches are found, null is returned.

```javascript
querySelector(selectors);
```

> Note that using this as an escape hatch to query by class or id is a bad practice because users can't see or identify these attributes. Use a testid if you have to.

## Jest API

### Globals

#### describe(name, fn)

`describe(name, fn)` creates a block that groups together several related tests.

#### test(name, fn, timeout)

under the alias: `it(name, fn, timeout)`

The first argument is the test name; the second argument is a function that contains the expectations to test. The third argument (optional) is timeout (in milliseconds) for specifying how long to wait before aborting.

### Expect - Methods

#### expect(value)

`expect(value)` gives access to a number of _matchers_ that let you validate different things.

#### .toBe(value)

Use .`toBe` to compare primitive values or to check referential identity of object instances.

#### .toHaveBeenCalled()

Also under the alias: `.toBeCalled()`

Use `.toHaveBeenCalled` to ensure that a mock function got called.

### jest-dom custom matchers

#### toBeInTheDocument

`toBeInTheDocument()` allows you to assert whether an element is present in the document or not.

> Note: This matcher does not find detached elements. The element must be added to the document to be found by toBeInTheDocument.

### Jest Mock Function

Mock functions are also known as "spies", because they let you spy on the behavior of a function that is called indirectly by some other code, rather than just testing the output. You can create a mock function with `jest.fn()`.

```javascript
const mockFn = jest.fn();
```

## Sources

[Paprika Getting Started](https://github.com/acl-services/paprika/wiki/Getting-Started)

[noop](https://whatis.techtarget.com/definition/no-op-no-operation)

[JavaScript | RegExp i Modifier](https://www.geeksforgeeks.org/javascript-regexp-i-modifier/)

[Accessibility - a11y](https://www.techopedia.com/definition/10165/accessibility-a11y)

[Document.querySelector()](https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelector)

[Testing Library Queries](https://testing-library.com/docs/dom-testing-library/api-queries)

[jest-dom custom matchers](https://github.com/testing-library/jest-dom#custom-matchers)

[Jest mock functions](https://jestjs.io/docs/en/jest-object.html#mock-functions)
