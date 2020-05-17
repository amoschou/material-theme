# material-theme
This is my attempt at creating a generic theme framework for MDC Web. Only colours are considered for now; other apects (shape, typography, etc.) are not (yet) dealt with here.

This project follows the principals outlined in the Theming Guide for MDC Web (https://github.com/material-components/material-components-web/blob/master/docs/theming.md).

The intention is that after defining the theme colours for a theme, components may be wrapped in a theme class and styles will be applied appropriately:

```<div class="theme-alpha">
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
</div>```


