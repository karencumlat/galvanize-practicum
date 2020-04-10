# Accessibility

## WAI-ARIA

[Web Accessibility Initiative - WAI](https://www.w3.org/WAI/standards-guidelines/aria/)

The Accessible Rich Internet Applications Suite, defines a way to make Web content and Web applications more accessible to people with disabilities. It especially helps with dynamic content and advanced user interface controls developed with Ajax, HTML, JavaScript, and related technologies.

## There are three main features defined in the spec:

[MDN - WAI-ARIA Basics](https://developer.mozilla.org/en-US/docs/Learn/Accessibility/WAI-ARIA_basics)

1. Roles — These define what an element is or does. Many of these are so-called landmark roles, which largely duplicate the semantic value of HTML5 structural elements e.g. role="navigation" `<nav>` or role="complementary" `<aside>`.

| Roles         |
| ------------- |
| navigation    |
| complementary |
| banner        |
| search        |
| tabgroup      |
| tab           |

2. Properties — These define properties of elements, which can be used to give them extra meaning or semantics. As an example, `aria-required="true"` specifies that a form input needs to be filled in to be valid, whereas `aria-labelledby="label"` allows you to put an ID on an element, then reference it as being the label for anything else on the page, including multiple elements, which is not possible using `<label for="input">`.
3. States — Special properties that define the current conditions of elements, such as aria-disabled="true", which specifies to a screenreader that a form input is currently disabled. States differ from properties in that properties don't change throughout the lifecycle of an app, whereas states can change, generally programmatically via JavaScript.

An important point about WAI-ARIA attributes is that they don't affect anything about the web page, except for the information exposed by the browser's accessibility APIs (where screenreaders get their information from). WAI-ARIA doesn't affect webpage structure, the DOM, etc., although the attributes can be useful for selecting elements by CSS.

### When should you use WAI-ARIA?

1. Signpost/Landmarks
2. Dynamic content updates
3. Enhancing keyboard accessibility
4. Accessibility of non-semantic controls
