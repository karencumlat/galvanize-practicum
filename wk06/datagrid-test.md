# DataGrid Test

## 1. Render DataGrid with ColumnHeader

```js
beforeEach(() => {
  ({ getByRole, getByText } = renderComponent());
});

it("should render a table with column", () => {
  expect(getByRole("grid")).toBeInTheDocument();
  expect(getByRole("columnheader")).toBeInTheDocument();
});
```

## 2. Render with Custom Content

```js
it("should render a table with custom content", () => {
  expect(getByRole("grid")).toBeInTheDocument();
  expect(getByText(/👋/i)).toBeInTheDocument();
});
```

## 3. Render DataGrid with StickyColumn

```js
const comp = "datagrid";
const testStory = "lazy--marvel-api-interaction";

beforeEach(() => {
  cy.visitStorybook(`${comp}-${testStory}`);
});

it("renders StickyColumn", () => {
  cy.get('[data-column-index="2"]')
    .eq(0)
    .then((e) => {
      const coords = e[0].getBoundingClientRect();

      cy.getAllByRole("rowgroup").last().scrollTo(100, 0);

      cy.get('[data-column-index="2"]')
        .eq(0)
        .then((e) => {
          const checkcoords = e[0].getBoundingClientRect();
          expect(checkcoords).to.deep.equal(coords);
        });
    });
});
```

### getBoundingClientRect()

The `Element.getBoundingClientRect()` method returns the size of an element and its position relative to the viewport.

Returns the following properties
left, top, right, bottom, x, y, width, and height

## 4. Render ColumnIndicator

```js
it("renders ColumnIndicator", () => {
  cy.get('[data-row-index="0"]')
    .eq(0)
    .children()
    .trigger("mouseover")
    .children()
    .should(($div) => {
      const className = $div[0].className;
      expect(className).to.match(/Checkbox/);
    });
});
```

## 5. Render ColumnExpand

```js
it("renders ColumnExpand", () => {
  cy.get('[data-row-index="0"]')
    .eq(1)
    .trigger("mouseover")
    .should("have.css", "opacity", "1");
});
```

## 6. Render `load more` button when you scroll to the bottom

```js
it("renders load more button when you scroll to the bottom", () => {
  cy.getAllByRole("rowgroup")
    .last()
    .scrollTo("bottom")
    .should("not.contain", "Amun");

  cy.get('[data-pka-anchor="button"').should("be.visible");
});
```

## 7. Navigate DataGrid `onkeyevents`

```js
const keyEvent = {
  enter: { keyCode: 13, which: 13, force: true },
  up: { keyCode: 38, which: 38, force: true },
  down: { keyCode: 40, which: 40, force: true },
};
```

### Key Down

The `keydown` event is fired when a key is pressed. It is fired for all keys, regardless of whether they produce a character value.

> While writing Cypress test for the DataGrid, `keydown` was used when arrow keys are pressed.d

```js
it("navigate DataGrid-collapsible OnArrowKeyDown", () => {
  cy.visitStorybook(`${comp}-lazy--collapse`);

  cy.getByText("Audit Planning").click();

  cy.getAllByText(/Narratives/i)
    .should("be.visible")
    .focused()
    .trigger("keydown", keyEvent.down)
    .focused()
    .trigger("keydown", keyEvent.down)
    .focused()
    .contains(/RCM/i);
});
```

### Key Up

the `keyup` event is fired when a key is released.

> `keyup` was used when `enter` key is pressed.

```js
it("navigate DataGrid-collapsible OnPressEnter", () => {
  cy.visitStorybook(`${comp}-lazy--collapse`);

  cy.getByText("Audit Planning")
    .click()
    .focused()
    .should("be.visible")
    .trigger("keydown", keyEvent.down)
    .focused()
    .trigger("keyup", keyEvent.enter)
    .getAllByText("Walkthrough")
    .should("be.visible");
});
```

## Sources

[Element.getBoundingClientRect](https://developer.mozilla.org/en-US/docs/Web/API/Element/getBoundingClientRect)

[Keydown event](https://developer.mozilla.org/en-US/docs/Web/API/Document/keydown_event)

[Keyup event](https://developer.mozilla.org/en-US/docs/Web/API/Document/keyup_event)
