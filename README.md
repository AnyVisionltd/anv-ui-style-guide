# AnyVision Style Guide

AnyVision theme and style guide library.

## Installation

Use the package manager npm.

```
npm i @anyvision/style-guide --save

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

### Colors
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
  --ac-sirius: #55efc4;
  --ac-canopus: #81ecec;
  --ac-vega: #74b9ff;
  --ac-rigel: #a29bfe;
  --ac-earth: #00b894;
  --ac-achernar: #00cec9;
  --ac-betelgeuse: #0984e3;
  --ac-agena: #6c5ce7;
  --ac-spica: #fd79a8;
  --ac-aldebaran: #ff7675;
  --ac-altair: #fab1a0;
  --ac-procyon: #ffeaa7;
  --ac-mimosa: #e84393;
  --ac-pollux: #d63031;
  --ac-antares: #e17055;
  --ac-sun: #fdcb6e;
}

```

### Space
```scss 
 :root {
  --micro: 4px;
  --tiny: 8px;
  --base: 16px;
  --medium: 24px;
  --loose: 32px;
  --large: 48px;
  --grand: 64px;
  --giant: 80px;
}
```

### Opacity
```scss 
 :root {
  --high: 1;
  --medium: 0.6;
  --disabled: 0.34;
  --divider: 0.12;
  --ghost: 0.05;
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

### opacity()
#### params
```
  high,
  medium,
  disabled,
  divider,
  ghost
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
