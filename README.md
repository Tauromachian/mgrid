# Grid System

This grid system is inspired by Bootstrap's layout system but utilizes CSS Grid. It is built with 12 columns, which can be spanned in various ways to create flexible layouts.

This module contains files that are fully modular. I don't offer a full bundle. So, if you want all the files you'll have to import them yourself.

## How to import

In a js file:

```js
import "@jogarcia/mgrid/container.scss";
import "@jogarcia/mgrid/g-row.scss";
import "@jogarcia/mgrid/g-col.scss";
import "@jogarcia/mgrid/gap.scss";
import "@jogarcia/mgrid/margin.scss";
import "@jogarcia/mgrid/padding.scss";
```

or

```js
import "@jogarcia/mgrid/dist/container.css";
import "@jogarcia/mgrid/dist/g-row.css";
import "@jogarcia/mgrid/dist/g-col.css";
import "@jogarcia/mgrid/dist/gap.css";
import "@jogarcia/mgrid/dist/margin.css";
import "@jogarcia/mgrid/dist/padding.css";
```

In a scss/sass file:

```scss
@import "~@jogarcia/mgrid/container.scss";
@import "~@jogarcia/mgrid/g-row.scss";
@import "~@jogarcia/mgrid/g-col.scss";
@import "~@jogarcia/mgrid/gap.scss";
@import "~@jogarcia/mgrid/margin.scss";
@import "~@jogarcia/mgrid/padding.scss";
```

or

```scss
@import "~@jogarcia/mgrid/dist/container.css";
@import "~@jogarcia/mgrid/dist/g-row.css";
@import "~@jogarcia/mgrid/dist/g-col.css";
@import "~@jogarcia/mgrid/dist/gap.css";
@import "~@jogarcia/mgrid/dist/margin.css";
@import "~@jogarcia/mgrid/dist/padding.css";
```

## Classes

- `.container`: Diminishes the spacing around the tag that its applied to.
- `.g-row`: Use this class for a grid row. It creates a grid layout context and contains 12 grid columns.
- `.g-col-{number}`: Spans {number} columns on from 0px on.
- `.g-col-{breakpoint}-{number}`: Spans {number} columns on from {breakpoint} on.
- `.gap-{number}`: Adds a gap with value {number}, uses the rem measure unit by default.
- `.m-{number}`: Adds margin in all directions. Uses the em measure unit by default.
- `.m{direction}-{number}`: Adds margin in the {direction} given.
- `.p-{number}`: Adds padding in all directions. Uses the em measure unit by default.
- `.p{direction}-{number}`: Adds padding in the {direction} given.

If you have used before most styles libraries you must be used to breakpoints. These are the default breakpoints of this library.

- xs: >= 0px
- sm: >= 576px
- md: >= 768px
- lg: >= 992px
- xl: >= 1200px
- 2xl:>= 1400px

Directions specified:

- t = top
- b = bottom
- l = left
- r = right
- x = right and left
- y = top and bottom
- If no specification = all the dimensions at the same time

## Customization

All the files posses customization options that can be changed at import.
This section defines each.

### Container

You can change the breakpoints of the container by passing them like this:

```scss
@use "~@jogarcia/mgrid/container.scss" with (
  $breakpoints: (
    "xs": (
      "min": 0px,
      "width": 100%,
    ),
    "sm": (
      "min": 576px,
      "width": 100%,
    ),
  )
);
```

### Row

Row does not have customization options

### Col

Similar to the container you can change the col breakpoints passing them like this:

```scss
@use "~@jogarcia/mgrid/g-col.scss" with (
  $breakpoints: (
    "xs": 0px,
    "sm": 476px,
    "md": 668px,
    "lg": 792px,
  )
);
```

### Gap, margin and padding

You can personalize the following variables in these 3:

- range. Defines how much classes there will be
- base. Allows you to multiply each iteration by this number. By default 1 for gap and 0.25 for margin and padding.
- unit. You can set your preferred unit. For gap I use rem while for margin and padding I use em.

An example with gap:

```scss
@use "~@jogarcia/mgrid/gap.scss" with (
  $base: 1,
  $range: 20,
  $unit: px
);
```

This will create gap classes from 0 to 20 using the pixels unit and multiplying each iteration with 1.
