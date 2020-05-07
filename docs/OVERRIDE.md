# Override
On this section you can see how to override the default values and theme CSS variables.


## Override Theme
Theme described with [Colors](VARIABLES.md#colors), [Spaces](VARIABLES.md#spaces) and [Border Radius](VARIABLES.md#radius).
<br/>
Colors the custom properties (variables) are in default define in ``:root`` element.
<br/>
To override the theme default colors, all need to do is create a CSS selector and 
<br/>
to define new CSS variables.
<br/>
<br/>

Do:
``` scss
:root {
  --primary: #{hexToRGBString(#3e7afc)};
  --secondary: #{hexToRGBString(#02234b)};
  --accent: 255, 255, 255;
  etc...
}

.my-theme {
  --primary: #{hexToRGBString(#3e7afc)};
  --secondary: #{hexToRGBString(#02234b)};
  --accent: 255, 255, 255;
  etc...
}
```
Dont: 
``` scss
:root {
  --primary: #3e7afc};
  --secondary: #{hexToRGBString(#NOTHEX)};
  --accent: rgb(255, 255, 255);
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

Do:
``` scss
// my-override-file.scss

$border-radius-types: (
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

Dont: 
``` scss
// my-override-file.scss

$border-radius-types: (
  tidy: 14,
  base: 18,
  round: 116,
  curvy: 124,
);
```
index.scss
``` scss
@import '~@anyvision/style-guide';
@import 'my-override-file';
```


On this way it will override `border-radius-sizes`.
