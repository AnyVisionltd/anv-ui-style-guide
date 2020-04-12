# Override
On this section you can see how to override the default values and theme CSS variables.


## Override Theme
Theme described with [Colors](VARIABLES.md#colors), [Spaces](VARIABLES.md#spaces) and [Border Radius](VARIABLES.md#radius).
<br/>
All the custom properties (variables) are in default define in ``:root`` element.
<br/>
To override the theme default colors, all need to do is create a CSS selector and 
<br/>
to define new CSS variables.
<br/>
<br/>
For example:

``` scss
:root {
  --secondary: #02234b;
  --primary: #3e7afc;
  --accent: #19e7fc;
  etc...
}

.my-spaces {
  --micro: 14px;
  --tiny: 18px;
  --base: 20px;
  etc...
}
```

## Override Default Values
To override the default value, need to create new file for example `my-override-file`.
<br/>
On this file need to declare SCSS variables with the same names as the default
<br/>
values.
<br/>
<br/>
For example:

``` scss
// my-override-file.scss

$border-radius-sizes: (
  tidy: 14,
  base: 18,
  round: 116,
  curvy: 124,
);
```
index.scss
``` scss
@import 'my-override-file';
@import '~@anyvision/style-guide';
```
On this way it will override `border-radius-sizes`.
