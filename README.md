# Simple container file class based on Bootstrap's class of the same type

This module provides a basic class. The class limits the content's width and adds margin to the sides.

## How to import

In a js file:

```js
import "mgrid/dist/container.css";
```

or

```js
import "mgrid/dist/container.css";
```

In a scss/sass file:

```scss
@import "~mgrid/container.scss";
```

or

```scss
@import "~mgrid/dist/container.scss";
```

## Default breakpoints

If you have used before most styles libraries you must be used so far to breakpoints. These are the default breakpoints of this library.

xs: >= 0px
sm: >= 576px
md: >= 768px
lg: >= 992px
xl: >= 1200px
2xl:>= 1400px

If you have worked with Bootstrap before you'll recognize this. These are Bootstrap's breakpoints.

## How to use

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

Additionally you can pass down you own breakpoints if you use SCSS. Example:

```scss
@use "~mgrid/container.scss" with (
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
