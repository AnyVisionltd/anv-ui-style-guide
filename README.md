# AnyVision Style Guide

AnyVision theme and style guide library.


## Contents
1. [Installation](#installation)
1. [Usage](#usage)
1. [Documentation](#documentation)

## Installation
Use the package manager npm.

```
npm i @anyvision/style-guide --save
```

## Usage
This library exports SCSS file!
```scss
@import '~@anyvision/style-guide';

.header { 
    background-color: av-color(trueblack);
}
```


## Documentation
The documentation is divided into several sections:

* [Override Theme](#override-theme)
* [Override Default Values](#override-default-values)
* [Functions](#functions)
* [Layout](#layout)


### Override Theme
Theme described with [Colors](#colors), [Spaces](#spaces) and [Border Radius](#border-radius).
<br/>
All the custom properties (variables) are in default define in ```:root``` element.
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

### Override Default Values
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

### Functions
This section will contain the available functions and the way to use them
<br/>
and their default value.
  
* [av-radius](#av-radius)
* [av-color](#av-color)
* [av-opacity](#av-opacity)
* [av-size](#av-size)
* [av-space](#av-space)
* [av-font-size](#av-font-size)
* [av-font-weight](#av-font-weight)

<hr/>

#### av-radius
This function will return the radius number value of the given parameter as CSS variable.
<br/>
Default value - `base`.
<br/>
<br/>
Available values - 

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
  border-radius: av-radius();abstracts
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

<hr/>

#### av-color
This function will return the color HEX of the given parameter as CSS variable.
<br/>
The function can get 2 parameters, the key of the requested color and the opacity.
<br/>
In case of using the opacity parameter the color value will be as RGBA.
<br/>
<br/>
Available values - 

```
primary: #3e7afc,
secondary: #02234b,
accent: #19e7fc,
decorative: #f43aac,
purewhite: #ffffff,
trueblack: #010a14,
surface1: #02244d,
surface2: #fafafc,
content1: #021d3d,
content2: #fcfeff,
success: #00d0a0,
alert: #ffc400,
error: #d50000,
ac-sirius: #55efc4,
ac-canopus: #81ecec,
ac-vega: #74b9ff,
ac-rigel: #a29bfe,
ac-earth: #00b894,
ac-achernar: #00cec9,
ac-betelgeuse: #0984e3,
ac-agena: #6c5ce7,
ac-spica: #fd79a8,
ac-aldebaran: #ff7675,
ac-altair: #fab1a0,
ac-procyon: #ffeaa7,
ac-mimosa: #ffeaa7,
ac-pollux: #d63031,
ac-antares: #e17055,
ac-sun: #fdcb6e
```  

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
<br/>

<hr/>

#### av-opacity
This function will return the opacity number value of the given parameter as CSS variable.
<br/>
<br/>
Available values- 

```
high: 1,
medium: 0.6,
disabled: 0.34,
divider: 0.12,
ghost: 0.05,
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

<hr/>

#### av-size
This function will return the size number value of the given parameter as CSS variable.
<br/>
<br/>
Available values- 

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

<hr/>

#### av-space
This function will return the space number value of the given parameter as CSS variable.
<br/>
Default value - `base`.
<br/>
<br/>
Available values - 

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
  padding: av-space();abstracts
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

<hr/>

#### av-font-size
This function will return the font size number value of the given as REM.
<br/>
Default value - `base`.
<br/>
<br/>
Available values - 

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

<hr/>

#### av-font-weight
This function will return the font weight number value of the given parameter.
<br/>
Default value - `normal`.
<br/>
<br/>
Available values - 

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
<br/>

