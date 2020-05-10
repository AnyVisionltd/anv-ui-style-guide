# Extensions
On this section will be  the documentation of the available extensions.
<br/>
<u><b>ALL THE EXTENSIONS MUST COME BEFORE THE IMPORT OF THE STYLE GUIDE!!</b></u>

* [Reset](#reset)
* [Normalize](#normalize)
* [av-normalize](#av-normalize)

How to `@import` all the extensions?

`@import '@anyvision/style-guide/extensions';`

## Reset
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

## Normalize
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

## av-normalize
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
