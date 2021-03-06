#center-me
---
Center me is a Handy little mixin that center's an element within its parent container. It uses the ```calc()``` function that is built in to CSS.

###Example Sass

```
  body {
    background-color: orange;
  }

  div {
    @include center-me(10em, 20em);
    background-color: blue;
  }
```

###Example CSS Output

```
  body {
    background-color: orange;
  }

  div {
    position: absolute;
    width: 20em;
    height: 10em;
    top: calc(50% - 5em);
    left: calc(50% - 10em);
    background-color: blue;
  }
```

###To Install
```
$ bower install center-me --save
```
In your Gruntfile.js (using grunt-sass):

```
sass: {
  dist: {
    files: {
      'application.css': 'sass/application.scss'
    },
    options: {
      includePaths: [
        './bower_components/center-me'
      ]
    }
  }
}
```
In your Sass manifest:

```
@import "center-me";
```
