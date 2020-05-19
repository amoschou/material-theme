# material-theme
This is my attempt at creating a generic theme framework for MDC Web. Only colours are considered for now; other apects (shape, typography, etc.) are not (yet) dealt with here.

This project follows the method outlined in the Theming Guide for MDC Web (https://github.com/material-components/material-components-web/blob/master/docs/theming.md).

The intention is that after defining the theme colours for a theme, components may be wrapped in a theme class and styles will be applied appropriately:

```html
<div class="theme-alpha">
  <div class="mdc-component">
    This component is styled using Theme Alpha’s colours.
  </div>
</div>

<div class="theme-beta">
  <div class="mdc-component">
    This component is styled using Theme Beta’s colours.
  </div>
</div>

<div class="theme-gamma">
  <div class="mdc-component">
    This component is styled using Theme Gamma’s colours.
  </div>
</div>
```

It is easy to apply a single set of colours to a global theme:
```scss
@use "@material/theme" with (
  $primary: #00838f,
  $secondary: #ff3d00,
  $background: $e0f7fa,
  $surface: $b2ebf2,
  $error: #d50000
);
@use "@material/button/mdc-button";
// etc
```
But Sass restricts how `@use` is used, and it can not be wrapped multiple times in a class.

This file demonstrates themes in the following way:
```scss
.theme-alpha {
  @include common-theme-work(
    $primary: #f44336,
    $secondary: #1565c0,
    $error: #d500f9,
    $background: #fff,
    $surface: #fff
  );
}

.theme-beta {
  @include common-theme-work(
    $primary: #3f51b5,
    $secondary: #00695c,
    $error: #00b0ff,
    $background: #fff,
    $surface: #fff
  );
}

.theme-gamma {
  @include common-theme-work(
    $primary: #009688,
    $secondary: #f9a825,
    $error: #76ff03,
    $background: #fff,
    $surface: #fff
  );
}
```
