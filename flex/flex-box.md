# CSS Flexbox

The CSS Flexbox layout mode provides a simple and flexible way to layout elements within a container. It allows you to align items in a row or a column, distribute space between them, and specify how elements should be sized to fit within the container.

## Key Concepts and Terms

### Flex container

An element that has the `display` property set to `flex` or `inline-flex` becomes a flex container. It contains flex items, which are its direct children.

```
.container {
	display: flex; /* or inline-flex */
}
```

### Flex item

An element that is a direct child of a flex container becomes a flex item. It can be thought of as a box that can be laid out within the flex container.

```
<div class="container">
	<div class="item">Item 1</div>
	<div class="item">Item 2</div>
	<div class="item">Item 3</div>
</div>
```

### Flex direction

The direction in which the flex items are laid out in the flex container. The default value is `row`, which means the items are laid out horizontally from left to right. Other possible values are `row-reverse`, which flips the order of the items horizontally, `column`, which lays out the items vertically from top to bottom, and `column-reverse`, which flips the order of the items vertically.

```
.container {
	display: flex;
	flex-direction: row; /* default value, lays out items horizontally from left to right. Other possible values: row-reverse, column, column-reverse */
}
```

### Justification

The alignment of the flex items along the main axis of the flex container. The main axis is the axis along which the flex items are laid out (horizontally for `row` or `row-reverse`, and vertically for `column` or `column-reverse`). The possible values for justification are `flex-start`, `flex-end`, `center`, `space-between`, and `space-around`.

```
.container {
	display: flex;
	justify-content: flex-start; /* default value, aligns items to the start of the main axis. Other possible values: flex-end, center, space-between, space-around */
}
```

### Alignment

The alignment of the flex items along the cross axis of the flex container. The cross axis is the axis perpendicular to the main axis. The possible values for alignment are `flex-start`, `flex-end`, `center`, `stretch`, and `baseline`.

```
.container {
	display: flex;
	align-items: flex-start; /* default value, aligns items to the start of the cross axis. Other possible values: flex-end, center, stretch, baseline */
}
```

### Flex grow and shrink

The `flex-grow` and `flex-shrink` properties allow you to specify how much a flex item should grow or shrink relative to the other items in the flex container. The `flex-grow` property specifies how much a flex item should grow relative to the remaining space in the flex container, while the `flex-shrink` property specifies how much it should shrink.

```
.item {
	flex-grow: 1; /* allows the item to grow as needed to fill remaining space in the container */
	flex-shrink: 1; /* allows the item to shrink as needed to fit within the container */
}
```

### Flex basis

The `flex-basis` property specifies the initial size of a flex item, before any growing or shrinking is applied. It can be specified in any unit of length (e.g., pixels, ems, etc.), or as a percentage of the size of the flex container.

```
.item {
	flex-basis: 200px; /* sets the initial width of the item to 200px */
}
```

## Properties

### display

The `display` property specifies the type of container an element should be. The possible values for this property are:

| Value         | Description                                                                          |
| ------------- | ------------------------------------------------------------------------------------ |
| `flex`        | The element becomes a flex container. Its direct children become flex items.         |
| `inline-flex` | The element becomes an inline flex container. Its direct children become flex items. |

### flex-direction

The `flex-direction` property specifies the direction in which the flex items are laid out in the flex container. The possible values for this property are:

| Value            | Description                                             |
| ---------------- | ------------------------------------------------------- |
| `row`            | The items are laid out horizontally from left to right. |
| `row-reverse`    | The items are laid out horizontally from right to left. |
| `column`         | The items are laid out vertically from top to bottom.   |
| `column-reverse` | The items are laid out vertically from bottom to top.   |

### flex-wrap

The `flex-wrap` property specifies whether the flex items should wrap onto multiple lines, or remain on a single line. The possible values for this property are:

| Value          | Description                                                                                        |
| -------------- | -------------------------------------------------------------------------------------------------- |
| `nowrap`       | The items will not wrap onto multiple lines. They will stay on a single line.                      |
| `wrap`         | The items will wrap onto multiple lines if necessary. The first item on each line is on the left.  |
| `wrap-reverse` | The items will wrap onto multiple lines if necessary. The first item on each line is on the right. |

### justify-content

The `justify-content` property aligns the flex items along the main axis of the flex container. The main axis is the axis along which the flex items are laid out (horizontally for `row` or `row-reverse`, and vertically for `column` or `column-reverse`). The possible values for this property are:

| Value           | Description                                                                          |
| --------------- | ------------------------------------------------------------------------------------ |
| `flex-start`    | The items are aligned to the start of the main axis.                                 |
| `flex-end`      | The items are aligned to the end of the main axis.                                   |
| `center`        | The items are aligned to the center of the main axis.                                |
| `space-between` | The items are evenly distributed along the main axis, with equal space between them. |
| `space-around`  | The items are evenly distributed along the main axis, with equal space around them.  |

### align-items

The `align-items` property aligns the flex items along the cross axis of the flex container. The cross axis is the axis perpendicular to the main axis. The possible values for this property are:

| Value        | Description                                                            |
| ------------ | ---------------------------------------------------------------------- |
| `flex-start` | The items are aligned to the start of the cross axis.                  |
| `flex-end`   | The items are aligned to the end of the cross axis.                    |
| `center`     | The items are aligned to the center of the cross axis.                 |
| `stretch`    | The items are stretched to fill the full height of the flex container. |
| `baseline`   | The items are aligned along their baselines.                           |

### align-self

The `align-self` property allows you to override the `align-items` property for a specific flex item. The possible values for this property are the same as those for `align-items`.

### flex-grow

The `flex-grow` property specifies how much a flex item should grow relative to the remaining space in the flex container. If all items have the same `flex-grow` value, the remaining space will be distributed equally among them. If some items have a higher `flex-grow` value than others, they will receive a larger share of the remaining space. The possible values for this property are any number, including decimals and negative numbers.

### flex-shrink

The `flex-shrink` property specifies how much a flex item should shrink relative to the other items in the flex container. If all items have the same `flex-shrink` value, they will all shrink at the same rate. If some items have a higher `flex-shrink` value than others, they will shrink more quickly. The possible values for this property are any number, including decimals and negative numbers.

### flex-basis

The `flex-basis` property specifies the initial size of a flex item, before any growing or shrinking is applied. It can be specified in any unit of length (e.g., pixels, ems, etc.), or as a percentage of the size of the flex container.

### flex

The `flex` shorthand property sets the `flex-grow`, `flex-shrink`, and `flex-basis` properties in a single declaration. The possible values for this property are:

| Syntax                                         | Description                                                                                              |
| ---------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| `flex: <flex-grow> <flex-shrink> <flex-basis>` | The `flex-grow`, `flex-shrink`, and `flex-basis` values are set to the provided values.                  |
| `flex: <flex-grow> <flex-shrink>`              | The `flex-grow` and `flex-shrink` values are set to the provided values, and `flex-basis` is set to `0`. |
| `flex: <flex-grow>`                            | The `flex-grow` value is set to the provided value, and `flex-shrink` and `flex-basis` are set to `1`.   |

### align-content

The `align-content` property aligns the flex lines within the flex container, when there are multiple lines. It is similar to `justify-content`, but it works on the cross axis instead of the main axis. The possible values for this property are:

| Value           | Description                                                                           |
| --------------- | ------------------------------------------------------------------------------------- |
| `flex-start`    | The lines are aligned to the start of the cross axis.                                 |
| `flex-end`      | The lines are aligned to the end of the cross axis.                                   |
| `center`        | The lines are aligned to the center of the cross axis.                                |
| `space-between` | The lines are evenly distributed along the cross axis, with equal space between them. |
| `space-around`  | The lines are evenly distributed along the cross axis, with equal space around them.  |
| `stretch`       | The lines are stretched to fill the full height of the flex container.                |

### order

The `order` property specifies the order of a flex item relative to the other items in the flex container. The possible values for this property are any integer, including negative numbers. Items with a lower `order` value will be placed before items with a higher `order` value.

### flex-flow

The `flex-flow` shorthand property sets the `flex-direction` and `flex-wrap` properties in a single declaration. The possible values for this property are:

| Syntax                                    | Description                                                                 |
| ----------------------------------------- | --------------------------------------------------------------------------- |
| `flex-flow: <flex-direction> <flex-wrap>` | The `flex-direction` and `flex-wrap` values are set to the provided values. |

## Demos

Below is an example of using Flexbox to layout a simple grid of items with fixed dimensions. This code will create a grid of items with a light blue background, a black border, and centered text. The items will be distributed evenly within the container, and will wrap to the next line when there is not enough space.

```
<!-- HTML -->
<div class="container">
	<div class="item">Item 1</div>
	<div class="item">Item 2</div>
	<div class="item">Item 3</div>
	<div class="item">Item 4</div>
	<div class="item">Item 5</div>
	<div class="item">Item 6</div>
</div>
```

```
/* CSS */
.container {
	display: flex;
	flex-wrap: wrap; /* allows items to wrap to the next line when there is not enough space */
	justify-content: space-around; /* distributes items evenly along the main axis */
}

.item {
	width: 200px;
	height: 200px;
	background-color: lightblue;
	border: 1px solid black;
	display: flex;
	align-items: center; /* centers items vertically within the container */
	justify-content: center; /* centers items horizontally within the container */
	font-size: 24px;
	font-weight: bold;
}
```

## Flexbox Versus Grid

CSS Flexbox and CSS Grid are both layout systems that allow you to position and size elements within a container. They can both be used to achieve a wide variety of layouts, but they have different strengths and are best suited to different types of tasks.

Some general guidelines for when to use Flexbox versus Grid:

* Use Flexbox when you want to lay out elements in a single dimension (either in a row or a column). Flexbox is particularly well-suited for laying out elements that need to be aligned along a single axis and distributed evenly within the container.
* Use Grid when you want to lay out elements in a two-dimensional grid. Grid is great for creating complex, multi-column layouts that require precise control over the placement of elements.

That being said, there is a lot of overlap between the two layout systems, and it is often possible to achieve similar layouts using either Flexbox or Grid. The choice between the two will often come down to personal preference, the specific requirements of your layout, and the trade-offs you are willing to make in terms of simplicity and flexibility.

It's worth noting that Flexbox is generally easier to learn and use than Grid, especially for simple layouts. However, Grid is more powerful and flexible, and is a better choice for more complex layouts that require precise control over element placement.

## Browser Compatibility
