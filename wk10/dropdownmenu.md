# DropdownMenu

## Issue: DropdownMenu does not scroll onOverflow

`<DropdownMenu/>` does not scroll when menu is overflowing off the screen

## Possible Solutions

- fix height for the menu
- prop to pass a height for the menu

Create a **new `maxHeight` prop** to stop the `<DropdownMenu/>` from overflowing off the screen and enable `overflow: auto`

> If the height of the menu prevents all the menu items from being displayed, setting a maxHeight will enable to scrolling

## Screenshots :camera:

### Issue behavior

![Overflowing DropDownMenu](../imgs/woScroll.gif)

### Solution behavior

![Scrollable DropDownMenu](../imgs/withScroll.gif)
