# AnyVision Style Guide

AnyVision theme and style guide library.

## Installation

Use the package manager npm.

```
npm i @anyvision/anv-ui-style-guide --save

```

## Usage

```scss
@import '~anv-ui-style-guide';

.header { 
    background-color: color(trueblack);
}

```

## Override & Theme
You have the ability to change the default values by set css variables.
``` scss
:root {
  --secondary: #02234b;
  --primary: #3e7afc;
  --accent: #19e7fc;
  --decorative: #f43aac;
  --purewhite: #ffffff;
  --surface1: #02244d;
  --surface2: #fafafc;
  --content1: #021d3d;
  --content2: #fcfeff;
  --trueblack: green;
  --success: #00d0a0;
  --alert: #ffc400;
  --error: #d50000;
}

```

## Available functions

### radius()
#### params
``` 
  tidy,
  base,
  round,
  curvy
```

### color()
#### params
``` 
  primary,
  secondary,
  accent,
  decorative,
  purewhite,
  trueblack,
  surface1,
  surface2,
  content1,
  content2,
  success,
  alert,
  error,
  ac-sirius,
  ac-canopus,
  ac-vega,
  ac-rigel,
  ac-earth,
  ac-achernar,
  ac-betelgeuse,
  ac-agena,
  ac-spica,
  ac-aldebaran,
  ac-altair,
  ac-procyon,
  ac-mimosa,
  ac-pollux,
  ac-antares,
  ac-sun
```

### size()
#### params
```
  sz-8,
  sz-16,
  sz-24,
  sz-32,
  sz-40,
  sz-48,
  sz-56,
  sz-64,
  sz-80,
  sz-96,
  sz-144,
  sz-240,
  sz-320,
  sz-480,
  sz-640,
  sz-960

``` 

### space()
#### params
```
  micro,
  tiny,
  base,
  medium,
  loose,
  large,
  grand,
  giant
```
