# Mixins
This section will contain the available mixins and the way to use them
<br/>
and their default value.

* [av-elevation](#av-elevation)

## av-elevation
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
