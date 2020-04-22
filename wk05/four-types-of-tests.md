# Static vs Unit vs Integration vs E2E Testing for Frontend Apps

![Testing Trophy](https://kentcdodds.com/static/c56de32357ab41ab66d6feb2dfaec567/00d43/testing-trophy.png)

## End to End

A helper robot that behaves like a user to click around the app and verify that it functions correctly. Sometimes called "functional testing" or e2e.

Typically these will run the entire application (both frontend and backend) and your test will interact with the app just like a typical user would. These tests are written with [cypress](https://www.cypress.io/).

## Integration

Verify that several units work together in harmony.

### Commands

#### visit

Visit a remote url

```jsx
cy.visit(url) // The URL to visit.

cy.visit('http://localhost:3000')    // Yields the window of the remote page
```

#### get

Get one or more DOM elements by selector or alias.

```jsx
cy.get(selector) // A selector used to filter matching DOM elements.
cy.get(alias) // An alias as defined using the .as() command and referenced with the @ character and the name of the alias.

cy.get('.list > li') // Yield the <li>'s in .list
```

#### click

Click a DOM element.

```jsx
.click()

cy.get('.btn').click()          // Click on button
```

#### should

Create an assertion. Assertions are automatically retried until they pass or time out.

```jsx
.should(chainers) // Any valid chainer that comes from Chai or Chai-jQuery or Sinon-Chai.
.should(chainers, value) // Value to assert against chainer

cy.get('.error').should('be.empty')
```

## Unit

Verify that individual, isolated parts work as expected.

## Static

Catch typos and type errors as you write the code.

## Sources

[Static vs Unit vs Integration vs E2E Testing for Frontend Apps](https://kentcdodds.com/blog/unit-vs-integration-vs-e2e-tests?ck_subscriber_id=363850105)