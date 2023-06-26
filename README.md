# Simple container file class based on Bootstrap's class of the same type

This module provides a basic class. The class limits the content's width and adds margin to the sides.

## How to import

In a js file:

```js
import "@jogarcia/mgrid/container.scss";
import "@jogarcia/mgrid/gap.scss";
import "@jogarcia/mgrid/margin.scss";
import "@jogarcia/mgrid/padding.scss";
```

or

```js
import "@jogarcia/mgrid/dist/container.css";
import "@jogarcia/mgrid/dist/gap.css";
import "@jogarcia/mgrid/dist/margin.css";
import "@jogarcia/mgrid/dist/padding.css";
```

In a scss/sass file:

```scss
@import "~@jogarcia/mgrid/container.scss";
@import "~@jogarcia/mgrid/gap.scss";
@import "~@jogarcia/mgrid/margin.scss";
@import "~@jogarcia/mgrid/padding.scss";
```

or

```scss
@import "~@jogarcia/mgrid/dist/container.css";
@import "~@jogarcia/mgrid/dist/gap.css";
@import "~@jogarcia/mgrid/dist/margin.css";
@import "~@jogarcia/mgrid/dist/padding.css";
```

## Container default breakpoints

If you have used before most styles libraries you must be used to breakpoints. These are the default breakpoints of this library.

xs: >= 0px
sm: >= 576px
md: >= 768px
lg: >= 992px
xl: >= 1200px
2xl:>= 1400px

If you have worked with Bootstrap before you'll recognize this. These are Bootstrap's breakpoints.

## How to use container

Add .container class to tag. Example:

```html
<div class="container">
  <h1>Test container</h1>
  <p>
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Praesentium
    suscipit velit repellat a blanditiis deleniti, culpa accusamus ducimus at.
  </p>
</div>
```

Additionally you can pass down your own breakpoints if you use SCSS. Example:

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

## Gap default values

By default the gap:

- Uses the rem unit.
- Iterates from 0 to 15 creating multiplying by a default base of 0.25.

```css
.gap-0 {
  gap: 0;
}

.gap-1 {
  gap: 0.25rem;
}

.gap-2 {
  gap: 0.5rem;
}
```

And so on until 15.

## Gap, how to use

The same as container you can directly use the class. In case you are using SCSS you can provide different range, base and unit.
Example:

```scss
@use "~@jogarcia/mgrid/gap.scss" with (
  $base: 1,
  $range: 20,
  $unit: px
);
```

This will create gap classes from 0 to 20 using the pixels unit and multiplying each iteration with 1.

## Margin and padding default values

By default both margin and padding:

- Use the em unit.
- Iterates from 0 to 15 creating multiplying by a default base of 1.
- Create dimensional classes where:
  - t = top
  - b = bottom
  - l = left
  - r = right
  - x = right and left
  - y = top and bottom
  - m = all the dimensions at the same time

```css
.mt-0 {
  margin-top: 0em;
}

.mt-1 {
  margin-top: 1em;
}

.mt-2 {
  margin-top: 2em;
}
```

And so on until 15 for every dimension.

Margin and padding also have the auto helper for all the dimensions.

## How to use

The same as gap you can directly use the class. In case you are using SCSS you can provide different range, base and unit.
Example:

```scss
@use "~@jogarcia/mgrid/gap.scss" with (
  $base: 1,
  $range: 20,
  $unit: px
);
```

This will create gap classes from 0 to 20 using the pixels unit and multiplying each iteration with 1.
