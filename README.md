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
1. [Usage](#usage)
1. [Documentation](#documentation)

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
import colors from '@anyvision/style-guide/abstracts/_colors.scss'
```

## fonts 
av-button:
  "fontSize": "14px"
  "fontWeight": 700
  "lineHeight": "0px"
  "textTransform": "uppercase"
  "letterSpacing": "1.34px"

av-body1:
  "fontSize": "16px"
  "fontWeight": 400
  "lineHeight": "24px"
  "letterSpacing": "0.44px"

av-body2: 
  "fontSize": "14px"
  "fontWeight": 400
  "lineHeight": "22px"
  "letterSpacing": "0.24px"

av-caption: 
  "fontSize": "12px"
  "fontWeight": 400
  "lineHeight": "16px"
  "letterSpacing": "0.4px"

av-headline1: 
  "fontSize": "96px"
  "fontWeight": 300
  "lineHeight": "145px"
  "letterSpacing": "-1.54px"

av-headline2: 
  "fontSize": "60px"
  "fontWeight": 300
  "lineHeight": "90px"
  "letterSpacing": "-0.48px"

av-headline3: 
  "fontSize": "48px"
  "fontWeight": 400
  "lineHeight": "0px"

av-headline4: 
  "fontSize": "32px"
  "fontWeight": 400
  "lineHeight": "51px"
  "letterSpacing": "0.26px"

av-headline5: 
  "fontSize": "24px",
  "fontWeight": 400,
  "lineHeight": "0px",

av-headline6: 
  "fontSize": "20px"
  "fontWeight": 600
  "lineHeight": "0px"
  "letterSpacing": "0.15px"

av-overline: 
  "fontSize": "10px"
  "fontWeight": 400
  "lineHeight": "0px"
  "textTransform": "uppercase"
  "letterSpacing": "1.5px"

av-subtitle1: 
  "fontSize": "16px"
  "fontWeight": 700
  "lineHeight": "0px"
  "letterSpacing": "0.14px"

av-subtitle2: 
  "fontSize": "14px"
  "fontWeight": 600
  "lineHeight": "24px"
  "letterSpacing": "0.1px"

## Documentation
The documentation is divided into several sections:

* [Override](docs/OVERRIDE.md)
* [Functions](docs/FUNCTIONS.md)
* [Layout](docs/LAYOUT.md)
* [Extensions](docs/EXTENSIONS.md)

