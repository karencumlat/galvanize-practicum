# Truncate

## Truncate in CSS

### Single Line

#### text-overflow

The `text-overflow` CSS property sets how hidden overflow content is signaled to users. It can be clipped, display an ellipsis ('…'), or display a custom string.

```css
overflow: hidden;
text-overflow: ellipsis;
white-space: nowrap;
```

### Line Clampin' (Truncating Multiple Line Text)

#### WebKit

```css
.line-clamp {
  display: -webkit-box;
  -webkit-line-clamp: 3;
  -webkit-box-orient: vertical;
}
```

> As of May 2020, `-webkit-line-clamp` is not supported by most browsers.

## Truncate in JavaScript

```js
function truncateString(str, num) {
  if (str.length <= num) {
    return str;
  }
  return str.slice(0, num) + "...";
}

truncateString("A-tisket a-tasket A green and yellow basket", 8);
```

## Sources

[css-tricks: text-overflow](https://css-tricks.com/almanac/properties/t/text-overflow/)

[mdn- text-over-flow](https://developer.mozilla.org/en-US/docs/Web/CSS/text-overflow)

[Truncate a string in JavaScript](https://medium.com/@dylanattal/truncate-a-string-in-javascript-41f33171d5a8)
