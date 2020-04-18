# Max Your Flex

Note that I have only compiled the flex-styles majorly used during flex development. This is not a complete documentation. Refer the following links for the complete documentation.

[Official MDN Resource for Flexbox](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox)

[CSS-Tricks Resource for Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

## How Flex Works
![alt text](https://css-tricks.com/wp-content/uploads/2018/11/00-basic-terminology.svg "Flex Architecture")

## Properties For Parent (flex-container)

#### display
```css
.container {
  display: flex; /* or inline-flex */
}
```

#### flex-direction
Check out the above architecture image to get more clarity.
```css
.container {
  flex-direction: row | row-reverse | column column-reverse;
}
```

#### flex-wrap
By default, flex items will all try to fit onto one line. You can change that and allow the items to wrap as needed with this property.
```css
.container {
  flex-wrap: nowrap | wrap | wrap-reverse;
}
```

#### flex-flow
This is a shorthand for the flex-direction and flex-wrap properties, which together define the flex container’s main and cross axes. The default value is row nowrap.
```css
.container {
  flex-flow: flex-direction; /* or flex-wrap */
}
```

#### justify-content
```css
.container {
  justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly;
}
```

#### align-items
```css
.container {
  align-items: stretch | flex-start | flex-end | center | baseline ;
}
```

#### align-content
```css
.container {
  align-content: flex-start | flex-end | center | space-between | space-around | space-evenly | stretch;
}
```

## Properties For Children (flex-items)

#### order
The order property controls the order in which they appear in the flex container.
```css
.item {
  order: 5; /* default is 0 */
}
```

#### flex-grow
This defines the ability for a flex item to grow if necessary.
```css
.item {
  flex-grow: 4; /* default 0 */
}
```

#### flex-shrink
This defines the ability for a flex item to shrink if necessary.
```css
.item {
  flex-shrink: 3; /* default 1 */
}
```

#### align-self
This allows the default alignment (or the one specified by align-items) to be overridden for individual flex items.
```css
.item {
  align-self: auto | flex-start | flex-end | center | baseline | stretch;
}
```

float, clear and vertical-align have no effect on a flex item.