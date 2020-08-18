# Anyvision Design System
This library design to make the user much more easier to work with the design system of Anyvision.
<br/>
<br/>
<b>What is the goal of this project?</b>
<br/>
<br/>
Now days to change the current application theme takes long time and because of that this repo became live.
<br/>
All you have to do now is just copy your new colors to you'r project and BOOM this works.


## Contents
1. [Installation](#installation)
2. [Usage](#usage)
3. [Functions & Mixins](#functions--mixins)
4. [Fonts](#fonts)
5. [Override](#override)
6. [Extensions](#extensions)
7. [Utils](#utils)

## Installation
Use the package manager npm.

```
npm i @anyvision/style-guide --save
```

## Usage
#### Access from scss
```scss
@import '~@anyvision/style-guide';

.header { 
    background-color: av-color(trueblack);
}
``` 

#### Access from js
```js
import colors from '@anyvision/style-guide'
```

## Functions & Mixins
This section will contain the available functions and the way to use them
<br/>
and their default value.

* [av-color](#av-color)  
* [av-opacity](#av-opacity)
* [av-size](#av-size)
* [av-space](#av-space)
* [av-font-size](#av-font-size)
* [av-font-weight](#av-font-weight)
* [av-elevation](#av-elevation)

### av-color
This function will return the color HEX of the given parameter as CSS variable.
<br/>
The function can get 2 parameters, the key of the requested color and the opacity.
<br/>
In case of using the opacity parameter the color value will be as RGBA.
<br/>

#### Values
##### Primary
Used to display the main colors of thee application
- ![#3e7afc](https://placehold.it/15/3e7afc/000000?text=+) `primary` - `#3e7afc` `rgb(62, 122, 252)`
- ![#02234b](https://placehold.it/15/02234b/000000?text=+) `secondary` - `#02234b` `rgb(2, 35, 75)`
- ![#19e7fc](https://placehold.it/15/19e7fc/000000?text=+) `accent` - `#19e7fc` `rgb(25, 231, 252)`
- ![#f43aac](https://placehold.it/15/f43aac/000000?text=+) `decorative` - `#f43aac` `rgb(244, 58, 172)`

##### Native
Used for native styles like shadow and etc...
- ![#ffffff](https://placehold.it/15/ffffff/000000?text=+) `purewhite` - `#ffffff` `rgb(255, 255, 255)`
- ![#010a14](https://placehold.it/15/010a14/000000?text=+) `trueblack` - `#010a14` `rgb(1, 10, 20)`

##### Content
Used in surfaces, Icons, Typography and any other UI elements
- ![#02244d](https://placehold.it/15/fcfcff/000000?text=+) `surface` - `#fcfcff` `rgb(255, 254, 254)`
- ![#fcfcff](https://placehold.it/15/021d3d/000000?text=+) `content` - `#021d3d` `rgb(2, 29, 61)`

##### Status
Used for showing the user the current status of a situation
- ![#00d0a0](https://placehold.it/15/00d0a0/000000?text=+) `success` - `#00d0a0` `rgb(0, 208, 160)`
- ![#ffc400](https://placehold.it/15/ffc400/000000?text=+) `alert` - `#ffc400` `rgb(255, 196, 0)`
- ![#d50000](https://placehold.it/15/d50000/000000?text=+) `error` - `#d50000` `rgb(213, 0, 0)`

##### Additional
Used for content differentiate (charts, watch lists, avatars...)
- ![#55efc4](https://placehold.it/15/55efc4/000000?text=+) `ac-sirius` - `#55efc4` `rgb(85, 239, 196)`
- ![#00b894](https://placehold.it/15/00b894/000000?text=+) `ac-earth` - `#00b894` `rgb(0, 184, 148)`
- ![#ffeaa7](https://placehold.it/15/ffeaa7/000000?text=+) `ac-procyon` - `#ffeaa7` `rgb(255, 234, 167)`
- ![#fdcb6e](https://placehold.it/15/fdcb6e/000000?text=+) `ac-sun` - `#fdcb6e` `rgb(253, 203, 110)`
- ![#81ecec](https://placehold.it/15/81ecec/000000?text=+) `ac-canopus` - `#81ecec` `rgb(129, 236, 236)`
- ![#00cec9](https://placehold.it/15/00cec9/000000?text=+) `ac-achernar` - `#00cec9` `rgb(0, 206, 201)`
- ![#fab1a0](https://placehold.it/15/fab1a0/000000?text=+) `ac-altair` - `#fab1a0` `rgb(250, 177, 160)`
- ![#e17055](https://placehold.it/15/e17055/000000?text=+) `ac-antares` - `#e17055` `rgb(225, 112, 85)`
- ![#74b9ff](https://placehold.it/15/74b9ff/000000?text=+) `ac-vega` - `#74b9ff` `rgb(116, 185, 255)`
- ![#0984e3](https://placehold.it/15/0984e3/000000?text=+) `ac-betelgeuse` - `#0984e3` `rgb(9, 132, 227)`
- ![#ff7675](https://placehold.it/15/ff7675/000000?text=+) `ac-aldebaran` - `#ff7675` `rgb(255, 118, 117)`
- ![#d63031](https://placehold.it/15/d63031/000000?text=+) `ac-pollux` - `#d63031` `rgb(214, 48, 49)`
- ![#a29bfe](https://placehold.it/15/a29bfe/000000?text=+) `ac-rigel` - `#a29bfe` `rgb(162, 155, 254)`
- ![#6c5ce7](https://placehold.it/15/6c5ce7/000000?text=+) `ac-agena` - `#6c5ce7` `rgb(108, 92, 231)`
- ![#fd79a8](https://placehold.it/15/fd79a8/000000?text=+) `ac-spica` - `#fd79a8` `rgb(253, 121, 168)`
- ![#e84393](https://placehold.it/15/e84393/000000?text=+) `ac-mimosa` - `#e84393` `rgb(232, 67, 147)`


Do:

```scss
.my-class {
  color: av-color(primary);// will return var(--primary, #3e7afc)
  background-color: av-color(secondary, opacity(ghost));// will return var(--secondary, rgba(2, 35, 75, var(--ghost, 0.05)))
  border-color: av-color(primary, .5);// will return var(--secondary, rgba(2, 35, 75, 0.5))
}
```

Dont:

```scss
.my-class {
  color: rgba(av-color(primary), .5);
}

.my-other-class {
  color: av-color(no-such-variable);// will throw compile error
}
```

### av-radius
This variables are manage to display the relevant `border-radius` as needed.
<br/>
The default value is in `px` to change the measure unit change the parameter `$border-radius-measure-unit`.
<br/>

Default value - `base`.

#### Values
```
tidy: 4,
base: 8,
round: 16,
curvy: 24,
```

Do:

```scss
.my-class {
  border-radius: av-radius(tidy);// will return var(--tidy, 4px)
}

.my-other-class {
  border-radius: av-radius();
}
```

Dont:

```scss
.my-class {
  width: av-radius(tidy);
}

.my-other-class {
  border-radius: av-radius(no-such-variable);
}
```
<br/>

### av-opacity
This function will return the opacity number value of the given parameter as CSS variable.
<br/>

#### Values 
```
high: 1,
medium: 0.6,
disabled: 0.34,
divider: 0.12,
ghost: 0.05
```
Do:

```scss
.my-class {
  opacity: av-opacity(ghost);// will return var(--ghost, 0.05)
  color: av-color(primary, av-opacity(ghost));// will return rgba(2, 35, 75, var(--ghost, 0.05))
}
```

Dont:

```scss
.my-class {
  opacity: av-opacity(no-such-variable);// will throw compile error
}
```
<br/>

### av-size
This variables are manage to display the relevant `width` as needed.
<br/>

#### Values

```
sz-8: 8,
sz-16: 16,
sz-24: 24,
sz-32: 32,
sz-40: 40,
sz-48: 48,
sz-56: 56,
sz-64: 64,
sz-80: 80,
sz-96: 96,
sz-144: 144,
sz-240: 240,
sz-320: 320,
sz-480: 480,
sz-640: 640,
sz-960: 960
```  

Do:

```scss
.my-class {
  width: av-size(sz-16);// will return var(--sz-16, 16px)
}
```

Dont: 

```scss
.my-class {
  height: av-size(sz-16);
  margin: av-size(sz-16);
  padding: av-size(sz-16);
}

.my-other-class {
  width: av-size(no-such-variable);// will throw compile error
}
```
<br/>

### av-space
This variables are manage to display the relevant `margin` or `padding` as needed.
<br/>
Default value - `base`.
<br/>
<br/>

#### Values
```
micro: 4,
tiny: 8,
base: 16,
medium: 24,
loose: 32,
large: 48,
grand: 64,
giant: 80
```

Do:

```scss
.my-class {
  margin: av-space(tiny);// will return var(--tiny, 8px)
  padding: av-space();
}
```

Dont: 

```scss
.my-class {
  width: av-space(tiny);
  height: av-space();
}

.my-other-class {
  width: av-space(no-such-variable);// will throw compile error
}
```
<br/>

### av-font-size
This function will return the font size number value of the given as REM.
<br/>
Default value - `base`.
<br/>

#### Values
```
micro: 10,
tiny: 12,
small: 14,
base: 16,
medium: 20,
large: 24,
x-large: 32,
grand: 48,
giant: 60,
header: 96
```

Do:

```scss
.my-class {
  font-size: av-font-size();// will return 1rem
}

.my-other-class {
  font-size: av-font-size(x-large);// will return 2rem
}
```

Dont: 

```scss
.my-class {
 font-size: av-font-size(no-such-variable);// will throw compile error
}
```
<br/>

### av-font-weight
This function will return the font weight number value of the given parameter.
<br/>
Default value - `normal`.
<br/>

#### Values
```
lighter: 300,
normal: 400,
bold: 700
```  

Do:

```scss
.my-class {
  font-weight: av-font-weight();// will return 400
}

.my-other-class {
  font-weight: av-font-weight(bold);// will return 700
}
```

Dont: 

```scss
.my-class {
 font-weight: av-font-weight(no-such-variable);// will throw compile error
}
```

### av-elevation
This mixin will return the relevant properties to the given elevation.
<br/>
By default this mixin will return `background-color: av-color(surface);` 
<br/>
even if the given elevation not exist.

Example: 
```scss
.my-class {
  @include av-elevation(); // this will return `background-color: av-color(surface);`
}

.my-other-class {
  @include av-elevation(pop-out);
  // will return -
  // background-color: var(--surface, rgba(2, 36, 77, 0.16));
  // box-shadow: 0 12px 24px 0 var(--trueblack, rgba(1, 10, 20, 0.1));
}
```

## Fonts 

Any text should use one of the fonts placeholders. 

Do:

```scss
.my-class {
  @extend %av-headline1;
}
```

Dont: 

```scss
.my-class {
 font-size: av-font-size(small);
 font-weight: av-font-weight(bold);
}
```

### Values

#### av-button 
```
 fontSize: 14px;
 fontWeight: 700;
 lineHeight: 0px;
 textTransform: uppercase;
 letterSpacing: 1.34px;
```

#### av-body1
```
 fontSize: 16px;
 fontWeight: 400;
 lineHeight: 24px;
 letterSpacing: 0.44px;
```


#### av-body2
```
 fontSize: 14px;
 fontWeight: 400;
 lineHeight: 22px;
 letterSpacing: 0.24px;
```

#### av-caption
```
 fontSize: 12px;
 fontWeight: 400;
 lineHeight: 16px;
 letterSpacing: 0.4px;
```

#### av-headline1
```
 fontSize: 96px;
 fontWeight: 300;
 lineHeight: 145px;
 letterSpacing: -1.54px;
```

#### av-headline2
```
 fontSize: 60px;
 fontWeight: 300;
 lineHeight: 90px;
 letterSpacing: -0.48px;
```

#### av-headline3
```
 fontSize: 48px;
 fontWeight: 400;
 lineHeight: 0;
```  

#### av-headline4
```
 fontSize: 32px;
 fontWeight: 400;
 lineHeight: 51px;
 letterSpacing: 0.26x;
```

#### av-headline5
```
 fontSize: 24px;
 fontWeight: 400;
 lineHeight: 0;
```

#### av-headline6
```
 fontSize: 20px;
 fontWeight: 600;
 lineHeight: 0;
 letterSpacing: 0.15x;
```

#### av-overline
```
 fontSize: 10px;
 fontWeight: 400;
 lineHeight: 0;
 letterSpacing: 1.5px;
 textTransform: uppercase;
```

#### av-subtitle1
```
 fontSize: 16px;
 fontWeight: 700;
 lineHeight: 0;
 letterSpacing: 1.14px;
```

#### av-subtitle1
```
 fontSize: 14px
 fontWeight: 600
 lineHeight: 24px
 letterSpacing: 0.1px
```


## Override
On this section you can see how to override the default values and theme CSS variables.


### Override Theme
Theme described with [Colors](VARIABLES.md#colors), [Spaces](VARIABLES.md#spaces) and [Border Radius](VARIABLES.md#radius).
<br/>
Colors the custom properties (variables) are in default define in ``:root`` element.
<br/>
To override the theme default colors, all need to do is create a CSS selector and 
<br/>
to define new CSS variables.
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

### Override Default Values
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

## Extensions
On this section will be  the documentation of the available extensions.
<br/>
<u><b>ALL THE EXTENSIONS MUST COME BEFORE THE IMPORT OF THE STYLE GUIDE!!</b></u>

* [Reset](#reset)
* [Normalize](#normalize)
* [av-normalize](#av-normalize)

How to `@import` all the extensions?

`@import '@anyvision/style-guide/extensions';`

### Reset
We use https://gist.github.com/DavidWells/18e73022e723037a50d6 CSS
<br/>
The goal of a reset stylesheet is to reduce browser inconsistencies in things like
<br/> 
default line heights, margins and font sizes of headings, and so on.

Do:
```scss
@import '@anyvision/style-guide/extensions/_reset.scss;
@import '@anyvision/style-guide';
```

Dont:
```scss
@import '@anyvision/style-guide';
@import '@anyvision/style-guide/extensions/_reset.scss;
```

### Normalize
We use https://necolas.github.io/normalize.css/
<br/>
Normalize.css makes browsers render all elements more consistently and in line
 <br/>
with modern standards. It precisely targets only the styles that need normalizing.

Do:
```scss
@import '@anyvision/style-guide/extensions/_normalize.scss;
@import '@anyvision/style-guide';
```

Dont:
```scss
@import '@anyvision/style-guide';
@import '@anyvision/style-guide/extensions/_normalize.scss;
```

### av-normalize
This is the common usages of the css styles in the Anyvision projects.

Do:
```scss
@import '@anyvision/style-guide/extensions/_av-normalize.scss;
@import '@anyvision/style-guide';
```

Dont:
```scss
@import '@anyvision/style-guide';
@import '@anyvision/style-guide/extensions/_av-normalize.scss;
```

## Utils

### set-as-var
This function will return the given key as `--key`.
<br/>
Use only to generate css variables!

Do:
```scss
// lets say $key = my-key
@function my-function($key) {
  $my-css-var: set-as-var($key);// will return --my-key
  //...
  @return var($my-css-var, #fff);
}
```

Dont:
```scss
// lets say $key = my-key
@function my-function($key) {
  $summary: set-as-var($key);
  //...
  @return $summary - 2px; 
}
```

### get-number
This function will return from a given map and a given key a number value
<br/>
and if the value is not a number the function will throw an error.

Do:
```scss
$my-map: (
  key1: 1,
  key2: '2'
);

// lets say $key = key1
@function my-function($key) {
  $my-css-var: get-number($my-map, $key);// will return 1
  //...
}
```

Dont:
```scss
$my-map: (
  key1: 1,
  key2: '2'
);

// lets say $key = key2
@function my-function($key) {
  $my-css-var: get-number($my-map, $key);// will throw an error
  //...
}
```

### rem
This function will return a px value as rem.

Do:
```scss
.my-class {
  font-size: rem(16px); //will return 1rem
}
```

Dont:
```scss
.my-class {
  font-size: rem(16cm); //will return 1rem
}
```

### hex-to-rgb-string
This function will return the red, green, blue values of an Hex color.

Do:
```scss
.my-class {
  --my-color: hex-to-rgb-string(#ffffff);
  --my-other-color: unquote(hex-to-rgb-string(#ffffff));
}
```

Dont:
```scss
.my-class {
  --my-color: hex-to-rgb-string(#not-hex-color);
}
```
