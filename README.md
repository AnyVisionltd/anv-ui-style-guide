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
* [av-z-index](#av-z-index)
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
- ![#3e7afc](https://via.placeholder.com/15/3e7afc/000000?text=+) `primary` - `#3e7afc` `rgb(62, 122, 252)`
- ![#02234b](https://via.placeholder.com/15/02234b/000000?text=+) `secondary` - `#02234b` `rgb(2, 35, 75)`
- ![#19e7fc](https://via.placeholder.com/15/19e7fc/000000?text=+) `accent` - `#19e7fc` `rgb(25, 231, 252)`
- ![#f43aac](https://via.placeholder.com/15/f43aac/000000?text=+) `decorative` - `#f43aac` `rgb(244, 58, 172)`

##### Native
Used for native styles like shadow and etc...
- ![#ffffff](https://via.placeholder.com/15/ffffff/000000?text=+) `purewhite` - `#ffffff` `rgb(255, 255, 255)`
- ![#010a14](https://via.placeholder.com/15/010a14/000000?text=+) `trueblack` - `#010a14` `rgb(1, 10, 20)`

##### Content
Used in surfaces, Icons, Typography and any other UI elements
- ![#02244d](https://via.placeholder.com/15/fcfcff/000000?text=+) `surface` - `#fcfcff` `rgb(255, 254, 254)`
- ![#fcfcff](https://via.placeholder.com/15/021d3d/000000?text=+) `content` - `#021d3d` `rgb(2, 29, 61)`

##### Status
Used for showing the user the current status of a situation
- ![#00d0a0](https://via.placeholder.com/15/00d0a0/000000?text=+) `success` - `#00d0a0` `rgb(0, 208, 160)`
- ![#13723D](https://via.placeholder.com/15/00d0a0/000000?text=+) `success-dark` - `#13723D` `rgb(19, 114, 61),`
- ![#ffc400](https://via.placeholder.com/15/ffc400/000000?text=+) `alert` - `#ffc400` `rgb(255, 196, 0)`
- ![#d50000](https://via.placeholder.com/15/d50000/000000?text=+) `error` - `#d50000` `rgb(213, 0, 0)`

##### Additional
Used for content differentiate (charts, watch lists, avatars...)
- ![#55efc4](https://via.placeholder.com/15/55efc4/000000?text=+) `ac-sirius` - `#55efc4` `rgb(85, 239, 196)`
- ![#00b894](https://via.placeholder.com/15/00b894/000000?text=+) `ac-earth` - `#00b894` `rgb(0, 184, 148)`
- ![#ffeaa7](https://via.placeholder.com/15/ffeaa7/000000?text=+) `ac-procyon` - `#ffeaa7` `rgb(255, 234, 167)`
- ![#fdcb6e](https://via.placeholder.com/15/fdcb6e/000000?text=+) `ac-sun` - `#fdcb6e` `rgb(253, 203, 110)`
- ![#81ecec](https://via.placeholder.com/15/81ecec/000000?text=+) `ac-canopus` - `#81ecec` `rgb(129, 236, 236)`
- ![#00cec9](https://via.placeholder.com/15/00cec9/000000?text=+) `ac-achernar` - `#00cec9` `rgb(0, 206, 201)`
- ![#fab1a0](https://via.placeholder.com/15/fab1a0/000000?text=+) `ac-altair` - `#fab1a0` `rgb(250, 177, 160)`
- ![#e17055](https://via.placeholder.com/15/e17055/000000?text=+) `ac-antares` - `#e17055` `rgb(225, 112, 85)`
- ![#74b9ff](https://via.placeholder.com/15/74b9ff/000000?text=+) `ac-vega` - `#74b9ff` `rgb(116, 185, 255)`
- ![#0984e3](https://via.placeholder.com/15/0984e3/000000?text=+) `ac-betelgeuse` - `#0984e3` `rgb(9, 132, 227)`
- ![#ff7675](https://via.placeholder.com/15/ff7675/000000?text=+) `ac-aldebaran` - `#ff7675` `rgb(255, 118, 117)`
- ![#d63031](https://via.placeholder.com/15/d63031/000000?text=+) `ac-pollux` - `#d63031` `rgb(214, 48, 49)`
- ![#a29bfe](https://via.placeholder.com/15/a29bfe/000000?text=+) `ac-rigel` - `#a29bfe` `rgb(162, 155, 254)`
- ![#6c5ce7](https://via.placeholder.com/15/6c5ce7/000000?text=+) `ac-agena` - `#6c5ce7` `rgb(108, 92, 231)`
- ![#fd79a8](https://via.placeholder.com/15/fd79a8/000000?text=+) `ac-spica` - `#fd79a8` `rgb(253, 121, 168)`
- ![#e84393](https://via.placeholder.com/15/e84393/000000?text=+) `ac-mimosa` - `#e84393` `rgb(232, 67, 147)`


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

Use Color Classes:
```html
<div className="text-primary ..."></div>
<div className="bg-primary ..."></div>
<div className="bg-secondary ..."></div>
<div className="bg-accent ..."></div>
<div className="bg-decorative ..."></div>
<div className="bg-purewhite ..."></div>
<div className="bg-trueblack ..."></div>
<div className="bg-surface ..."></div>
<div className="bg-content ..."></div>
<div className="bg-success ..."></div>
<div className="bg-alert ..."></div>
<div className="bg-error ..."></div>
<div className="bg-sirius ..."></div>
<div className="bg-earth ..."></div>
<div className="bg-procyon ..."></div>
<div className="bg-sun ..."></div>
<div className="bg-canopus ..."></div>
<div className="bg-achernar ..."></div>
<div className="bg-altair ..."></div>
<div className="bg-antares ..."></div>
<div className="bg-vega ..."></div>
<div className="bg-betelgeuse ..."></div>
<div className="bg-aldebaran ..."></div>
<div className="bg-pollux ..."></div>
<div className="bg-rigel ..."></div>
<div className="bg-agena ..."></div>
<div className="bg-spica ..."></div>
```

Use Color with Styled Components
```tsx
import tw from "tailwind-styled-components"

const StyledText = tw.div`
  text-primary
  bg-purewhite
`
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

Use Radius Classes:
```html
<!-- tidy 4px 0.25rem -->
<div className="rounded ..."></div>

<!-- base 8px 0.5rem -->
<div className="rounded-lg ..."></div> 

<!-- round 16px 1rem -->
<div className="rounded-2xl ..."></div> 

<!-- curvy 24px 1.5rem -->
<div className="rounded-3xl ..."></div> 

```

Use Radius with Styled Components
```tsx
import tw from "tailwind-styled-components"

const StyledText = tw.div`
  rounded
`
```


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

Use Opacity Classes:
```html
<div className="opacity-high ..."></div>
<div className="opacity-medium ..."></div>
<div className="opacity-disabled ..."></div>
<div className="opacity-divider ..."></div>
<div className="opacity-ghost ..."></div>
```

Use Opacity with Styled Components
```tsx
import tw from "tailwind-styled-components"

const StyledText = tw.div`
  opacity-disabled
`
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

Use Size Classes:
```html
<!-- width -->
<div className="w-4 ..."></div>
<div className="w-8 ..."></div>
<div className="w-16 ..."></div>
<div className="w-24 ..."></div>
<div className="w-32 ..."></div>
<div className="w-40 ..."></div>
<div className="w-48 ..."></div>
<div className="w-56 ..."></div>
<div className="w-64 ..."></div>
<div className="w-80 ..."></div>
<div className="w-96 ..."></div>
<div className="w-144 ..."></div>
<div className="w-240 ..."></div>
<div className="w-320 ..."></div>
<div className="w-480 ..."></div>
<div className="w-640 ..."></div>
<div className="w-960 ..."></div>


<!-- min-width -->
<div className="min-w-16 ..."></div>
<!-- max-width -->
<div className="max-w-16 ..."></div>
<!-- height -->
<div className="h-16 ..."></div>

<!-- padding -->
<div className="p-16 ..."></div>
<!-- padding x axis (left, right) -->
<div className="px-16 ..."></div>
<!-- padding y axis (top, bottom) -->
<div className="py-16 ..."></div>

<!-- margin -->
<div className="m-16 ..."></div>

<div className="flex space-x-16 ...">
  <div>01</div>
  <div>02</div>
  <div>03</div>
</div>

```

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

### av-z-index
this function will return relevant z-indexes.
<br/>
<br/>

#### Values
```
  raised: 1,
  navigation: 10,
  popup: 20,
  notification: 30,
  important: 40
```

Do:

```scss
.my-class {
  z-index: av-z-index(raised);
}
```

Use Z-Index Classes:
```html
<div className="z-raised ..."></div>
<div className="z-navigation ..."></div>
<div className="z-popup ..."></div>
<div className="z-notification ..."></div>
<div className="z-important ..."></div>
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
header: 96,
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










Use Font Size Classes:
```html
<p className="text-micro ...">The quick brown fox ...</p>  <!-- 10px -->
<p className="text-tiny ...">The quick brown fox ...</p> <!-- 12px -->
<p className="text-sm ...">The quick brown fox ...</p> <!-- 14px -->
<p className="text-base ...">The quick brown fox ...</p> <!-- 16px -->
<p className="text-md ...">The quick brown fox ...</p> <!-- 20px -->
<p className="text-lg ...">The quick brown fox ...</p> <!-- 24px -->
<p className="text-xl ...">The quick brown fox ...</p> <!-- 32px -->
<p className="text-2xl ...">The quick brown fox ...</p> <!-- 48px -->
<p className="text-3xl ...">The quick brown fox ...</p> <!-- 60px -->
<p className="text-header ...">The quick brown fox ...</p> <!-- 96px -->
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

Use Font Weight Classes:
```html
<p className="font-light ...">The quick brown fox ...</p> <!-- 300 -->
<p className="font-normal ...">The quick brown fox ...</p> <!-- 400 -->
<p className="font-bold ...">The quick brown fox ...</p> <!-- 700 -->
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

```tsx
const StyledButton = tw.button`
  text-sm
  font-bold
  leading-[0px]
  uppercase
  tracking-[1.34px]
`
```

#### av-body1
```
 fontSize: 16px;
 fontWeight: 400;
 lineHeight: 24px;
 letterSpacing: 0.44px;
```

```tsx
const StyledBody1 = tw.span`
  text-base
  font-normal
  leading-[24px]
  tracking-[0.44px]
`
```

#### av-body2
```
 fontSize: 14px;
 fontWeight: 400;
 lineHeight: 22px;
 letterSpacing: 0.24px;
```

```tsx
const StyledBody2 = tw.span`
  text-sm
  font-normal
  leading-[22px]
  tracking-[0.24px]
`
```

#### av-caption
```
 fontSize: 12px;
 fontWeight: 400;
 lineHeight: 16px;
 letterSpacing: 0.4px;
```

```tsx
const StyledCaption = tw.span`
  text-tiny
  font-normal
  leading-[16px]
  tracking-[0.4px]
`
```

#### av-headline1
```
 fontSize: 96px;
 fontWeight: 300;
 lineHeight: 145px;
 letterSpacing: -1.54px;
```

```tsx
const StyledH1 = tw.span`
  text-header
  font-light
  leading-[145px]
  tracking-[-1.54px]
`
```

#### av-headline2
```
 fontSize: 60px;
 fontWeight: 300;
 lineHeight: 90px;
 letterSpacing: -0.48px;
```

```tsx
const StyledH2 = tw.span`
  text-3xl
  font-light
  leading-[90px]
  tracking-[-0.48px]
`
```

#### av-headline3
```
 fontSize: 48px;
 fontWeight: 400;
 lineHeight: 0;
```  

```tsx
const StyledH3 = tw.span`
  text-2xl
  font-normal
  leading-[0]
`
```

#### av-headline4
```
 fontSize: 32px;
 fontWeight: 400;
 lineHeight: 51px;
 letterSpacing: 0.26x;
```

```tsx
const StyledH4 = tw.span`
  text-xl
  font-normal
  leading-[51px]
  tracking-[0.26px]
`
```

#### av-headline5
```
 fontSize: 24px;
 fontWeight: 400;
 lineHeight: 0;
```

```tsx
const StyledH5 = tw.span`
  text-lg
  font-normal
  leading-[0]
`
```

#### av-headline6
```
 fontSize: 20px;
 fontWeight: 600;
 lineHeight: 0;
 letterSpacing: 0.15x;
```

```tsx
const StyledH6 = tw.span`
  text-md
  font-semibold
  leading-[0]
  tracking-[0.15px]
`
```

#### av-overline
```
 fontSize: 10px;
 fontWeight: 400;
 lineHeight: 0;
 letterSpacing: 1.5px;
 textTransform: uppercase;
```

```tsx
const StyledOverline = tw.span`
  text-micro
  font-normal
  leading-[0]
  tracking-[1.5px]
  uppercase
`
```

#### av-subtitle1
```
 fontSize: 16px;
 fontWeight: 700;
 lineHeight: 0;
 letterSpacing: 1.14px;
```

```tsx
const StyledSubtitle1 = tw.span`
  text-base
  font-bold
  leading-[0]
  tracking-[1.14px]
`
```

#### av-subtitle2
```
 fontSize: 14px
 fontWeight: 600
 lineHeight: 24px
 letterSpacing: 0.1px
```

```tsx
const StyledSubtitle2 = tw.span`
  text-sm
  font-semibold
  leading-[24px]
  tracking-[0.1px]
`
```





## Override
On this section you can see how to override the default values and theme CSS variables.

### Set the default color system
Import colors and set the css variables to defaults
```scss
@import '~@anyvision/style-guide';
// Set default colors on :root element
:root {
  @each $key, $value in $color-palate {
    #{set-as-var($key)}: unquote(hex-to-rgb-string($value));
  }
}
```

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
  --primary: #{hex-to-rgb-string(#3e7afc)};
  --secondary: #{hex-to-rgb-string(#02234b)};
  --accent: 255, 255, 255;
  etc...
}

.my-theme {
  --primary: #{hex-to-rgb-string(#3e7afc)};
  --secondary: #{hex-to-rgb-string(#02234b)};
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
