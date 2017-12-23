# stylepkg

A set of base styles and SASS mixins commonly used in my projects.

## Mixins

**Breakpoints**

The following breakpoint variables are available:

```scss
$breakpoint-xs: 480px;
$breakpoint-sm: 600px;
$breakpoint-md: 840px;
$breakpoint-lg: 960px;
$breakpoint-xl: 1280px;
```

There is also a `$breakpoints` map that can be accessed like so:

```scss
$breakpoints('xs') // $breakpoint-xs
$breakpoints('sm') // $breakpoint-sm
$breakpoints('md') // $breakpoint-md
$breakpoints('lg') // $breakpoint-lg
$breakpoints('xl') // $breakpoint-xl
```

**min-width(breakpoint)**

A simple responsive breakpoint mixin to apply styles above a specified breakpoint. Accepts any of the breakpoints defined above.

Example:

```scss
.header {
  font-size: 2rem;

  @include min-width("lg") {
    font-size: 1.625rem;
  }
}
```

**max-width(breakpoint)**

A simple responsive breakpoint mixin to apply styles below a specified breakpoint. Accepts any of the breakpoints defined above.

Example:

```scss
.header {
  font-size: 2rem;

  @include max-width("lg") {
    font-size: 1.625rem;
  }
}
```
