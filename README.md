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


## Documentation
The documentation is divided into several sections:

* [Override](docs/OVERRIDE.md)
* [Functions](docs/FUNCTIONS.md)
* [Layout](docs/LAYOUT.md)
* [Extensions](docs/EXTENSIONS.md)

