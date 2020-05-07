# Functions
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
* [set-as-var](#set-as-var)
* [get-number](#get-number)
* [rem](#rem)
* [hex-to-rgb-string](#hex-to-rgb-string)

## av-radius
This function will return the radius number value of the given parameter as CSS variable.
<br/>
Default value - `base`.

[Available Values](VARIABLES.md#radius)

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

## av-color
This function will return the color HEX of the given parameter as CSS variable.
<br/>
The function can get 2 parameters, the key of the requested color and the opacity.
<br/>
In case of using the opacity parameter the color value will be as RGBA.
<br/>
<br/>
[Available Values](VARIABLES.md#colors)

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

## av-opacity
This function will return the opacity number value of the given parameter as CSS variable.
<br/>
<br/>
[Available Values](VARIABLES.md#opacity)


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

## av-size
This function will return the size number value of the given parameter as CSS variable.
<br/>
<br/>
[Available Values](VARIABLES.md#sizes)

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

## av-space
This function will return the space number value of the given parameter as CSS variable.
<br/>
Default value - `base`.
<br/>
<br/>
[Available Values](VARIABLES.md#spaces) 

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

## av-font-size
This function will return the font size number value of the given as REM.
<br/>
Default value - `base`.
<br/>
<br/>
[Available Values](VARIABLES.md#font-sizes)

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

## av-font-weight
This function will return the font weight number value of the given parameter.
<br/>
Default value - `normal`.
<br/>
<br/>
[Available Values](VARIABLES.md#font-weight)

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

## set-as-var
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

## get-number
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

## rem
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

## hex-to-rgb-string
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
