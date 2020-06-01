# Card

![Card](../imgs/card.PNG)

## Create sub-components

```js
<Card>
  <Card.Body>
    <Card.Icon>
      <Icon>
    </Card.Icon>
    <Card.Title>
      <Heading>
    </Card.Title>
    <Card.Meta/>
    <Card.Content/>
  </Card.Body>

  <Card.Footer>
  </Card.Footer>

</Card>
```

```js
<Card>
  <Card.Body>
    props={
      cardIcon: initial
      cardTitle: required
      cardMetadata:
      cardContent:
    }
  </Card.Body>

  <Card.Footer>props:</Card.Footer>
</Card>
```

## Props

- width: 280px, 25%, 33%, 50%, 100%

  - maxWidth
  - minWidth

```js
import

const propTypes ={}

const defaultProps = {}

function Card (props){
  const  {} = props;
  return();
}

Card.displayName = "Card";
Card.propTypes = propTypes;
Card.defaultProps = defaultProps;

export default Counter;
```

## Discussion with Nahum

```js

export const = Card.div`
  width: 120px;
  min-height: 120px;
`

```

<Card> // Div wrapper that either is full width or has a defaultWidth

```jsx
<Card>
  <Card.Content>
    <Card.Header>
      <Avatar />
      <DropDownMenu />
    </Card.Header>
    <Card.Separator space={1} /> {/* height space*/}
    <Card.Title>My Policy 🎉</Card.Title>
    <Card.MetaData>
      <span>1000 assets</span>
    </Card.MetaData>
  </Card.Content>
  <Card.Footer>{children}<Card.Footer>
</Card>

// ✅ testing, screener. 🙅‍♀️ cypress/reacting/testing
// to create screener test just add .screener suffix to your story file ex:
`MyFile.screener.stories.js`

<Card.Task label="string" pill="string">


// Create a new component name Avatar
<Avatar>
```

```jsx
<Card>
  <Avatar />
  <Card.Title>Second robot</Card.Title>
  <Card.Metadata>No activated version</Card.Metadata>
  <Card.Text>
    This is the robot description. we will display 2-3 lines and then truncate
    the remainder...
  </Card.Text>
  <Card.Footer>
    <ConsumerComponent />
  </Card.Footer>
</Card>
```

## To Do Components

1. Card
2. Header
3. Avatar
4. Content
5. Title
6. Metadata
7. Text
8. Footer

### Avatar

```jsx
import React from "react";
import PropTypes from "prop-types";

const propTypes = {
  children: PropTypes.node,
  color: PropTypes.oneOf([]), // check counter
  size: PropTypes.oneOf(ShirtSizes.LIMITED),
};

const defaultProps = {
  children: null,
  color: "",
  size: "",
};

export default function Avatar(props) {
  const { color, size, children } = props;

  const AvatarProps = {
    color,
    size,
    children,
  };
  return <span data-pka-anchor="avatar" css={avatarStyles}></span>;
}

Avatar.displayName = "Avatar";
Avatar.propTypes = propTypes;
Avatar.defaultProps = defaultProps;

export default Avatar;
```
