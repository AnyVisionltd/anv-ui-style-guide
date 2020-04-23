# Variables 
Each section will contain the current variable default values.
<br/>
Also each variable is exported to the js and the variable you can override.


## Colors
This system designed to be consistent, harmonious, ensure accessible text, and distinguish UI elements and surfaces from one another.
<br/>
To change the default colors value map override `$color-palate` map.
<br/>

Import exported variables in thr JavaScript file -
<br/>
`import colors from '@anyvision/style-guide/abstracts/_colors.scss'` 

#### Primary
Used to display the main colors of thee application
- ![#3e7afc](https://placehold.it/15/3e7afc/000000?text=+) `primary - #3e7afc`
- ![#02234b](https://placehold.it/15/02234b/000000?text=+) `secondary - #02234b`
- ![#19e7fc](https://placehold.it/15/19e7fc/000000?text=+) `accent - #19e7fc`
- ![#f43aac](https://placehold.it/15/f43aac/000000?text=+) `decorative - #f43aac`

#### Native
Used for native styles like shadow and etc...
- ![#ffffff](https://placehold.it/15/ffffff/000000?text=+) `purewhite - #ffffff`
- ![#010a14](https://placehold.it/15/010a14/000000?text=+) `trueblack - #010a14`

#### Content
Used in surfaces, Icons, Typography and any other UI elements
- ![#02244d](https://placehold.it/15/02244d/000000?text=+) `surface - #02244d`
- ![#fcfcff](https://placehold.it/15/fcfcff/000000?text=+) `content - #fcfcff`

#### Status
Used for showing the user the current status of a situation
- ![#00d0a0](https://placehold.it/15/00d0a0/000000?text=+) `success - #00d0a0`
- ![#ffc400](https://placehold.it/15/ffc400/000000?text=+) `alert - #ffc400`
- ![#d50000](https://placehold.it/15/d50000/000000?text=+) `error - #d50000`

#### Additional
Used for content differentiate (charts, watch lists, avatars...)
- ![#55efc4](https://placehold.it/15/55efc4/000000?text=+) `ac-sirius - #55efc4`
- ![#00b894](https://placehold.it/15/00b894/000000?text=+) `ac-earth - #00b894`
- ![#ffeaa7](https://placehold.it/15/ffeaa7/000000?text=+) `ac-procyon - #ffeaa7`
- ![#fdcb6e](https://placehold.it/15/fdcb6e/000000?text=+) `ac-sun - #fdcb6e`
- ![#81ecec](https://placehold.it/15/81ecec/000000?text=+) `ac-canopus - #81ecec`
- ![#00cec9](https://placehold.it/15/00cec9/000000?text=+) `ac-achernar - #00cec9`
- ![#fab1a0](https://placehold.it/15/fab1a0/000000?text=+) `ac-altair - #fab1a0`
- ![#e17055](https://placehold.it/15/e17055/000000?text=+) `ac-antares - #e17055`
- ![#74b9ff](https://placehold.it/15/74b9ff/000000?text=+) `ac-vega - #74b9ff`
- ![#0984e3](https://placehold.it/15/0984e3/000000?text=+) `ac-betelgeuse - #0984e3`
- ![#ff7675](https://placehold.it/15/ff7675/000000?text=+) `ac-aldebaran - #ff7675`
- ![#d63031](https://placehold.it/15/d63031/000000?text=+) `ac-pollux - #d63031`
- ![#a29bfe](https://placehold.it/15/a29bfe/000000?text=+) `ac-rigel - #a29bfe`
- ![#6c5ce7](https://placehold.it/15/6c5ce7/000000?text=+) `ac-agena - #6c5ce7`
- ![#fd79a8](https://placehold.it/15/fd79a8/000000?text=+) `ac-spica - #fd79a8`
- ![#e84393](https://placehold.it/15/e84393/000000?text=+) `ac-mimosa - #e84393`

## Radius
This variables are manage to display the relevant `border-radius` as needed.
<br/>
The default value is in `px` to change the measure unit change the parameter `$border-radius-measure-unit`.
<br/>

Import exported variables in thr JavaScript file -
<br/>
`import colors from '@anyvision/style-guide/abstracts/_border-radius.scss'` 

```
tidy: 4,
base: 8,
round: 16,
curvy: 24,
```

## Opacity
This system design make used to determinate which element is higher then the other.
<br/>
To override the default values use `$opacity-types`.
<br/>

Import exported variables in thr JavaScript file -
<br/>
`import colors from '@anyvision/style-guide/abstracts/_opacity.scss'` 

```
high: 1,
medium: 0.6,
disabled: 0.34,
divider: 0.12,
ghost: 0.05
```  

## Shadows
This system describe how much shadow the element should have.
<br/>
To override the default values use `$shadow-types`.
<br/>

Import exported variables in thr JavaScript file -
<br/>
`import colors from '@anyvision/style-guide/abstracts/_shadows.scss'` 

```
micro: 0 1px 2px 0,
tiny: 0 4px 8px 0,
small: 0 6px 10px 0,
medium: 0 8px 16px 0,
large: 0 12px 24px 0,
```

## Sizes
This variables are manage to display the relevant `width` as needed.
<br/>
To override the default values use `$sizes-types`.
<br/>
The default value is in `px` to change the measure unit change the parameter `$sizes-measure-unit`.
<br/>

Import exported variables in thr JavaScript file -
<br/>
`import colors from '@anyvision/style-guide/abstracts/_sizes.scss'` 

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

## Spaces
This variables are manage to display the relevant `margin` or `padding` as needed.
<br/>
To override the default values use `$spacing-sizes`.
<br/>
The default value is in `px` to change the measure unit change the parameter `$spacing-measure-unit`.
<br/>

Import exported variables in thr JavaScript file -
<br/>
`import colors from '@anyvision/style-guide/abstracts/_spaces.scss'` 

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

#### Font Sizes
This variables are manage to display the relevant `font-size` as needed.
<br/>
To override the default values use `$font-sizes`.
<br/>

Import exported variables in thr JavaScript file -
<br/>
`import colors from '@anyvision/style-guide/abstracts/_typography.scss'` 

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

#### Font Weight
This variables are manage to display the relevant `font-width` as needed.
<br/>
To override the default values use `$font-weight`.
<br/>

Import exported variables in thr JavaScript file -
<br/>
`import colors from '@anyvision/style-guide/abstracts/_typography.scss'` 

```
lighter: 300,
normal: 400,
bold: 700
```  
