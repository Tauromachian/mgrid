# Simple container file class based on Bootstrap's class of the same type

This module provides a basic class. The class limits the content's width and adds margin to the sides.

## How to import

In a js file:

```js
import "@jogarcia/mgrid/container.scss";
import "@jogarcia/mgrid/gap.scss";
```

or

```js
import "@jogarcia/mgrid/dist/container.css";
import "@jogarcia/mgrid/dist/gap.css";
```

In a scss/sass file:

```scss
@import "~@jogarcia/mgrid/container.scss";
@import "~@jogarcia/mgrid/gap.scss";
```

or

```scss
@import "~@jogarcia/mgrid/dist/container.css";
@import "~@jogarcia/mgrid/dist/gap.css";
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
