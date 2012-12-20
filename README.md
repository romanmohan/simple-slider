# Gdoc Powered Slider

A mobile friendly slider created from a google spreadsheet. Requires tabletop and jquery

## Getting Started
Download the [production version][min] or the [development version][max].

[min]: https://raw.github.com/motherjones/gdoc-powered-slider/master/dist/gdoc-powered-slider.min.js
[max]: https://raw.github.com/motherjones/gdoc-powered-slider/master/dist/gdoc-powered-slider.js

In your web page:

```html
<script src="jquery.js"></script>
<script src="libs/tabletop.js"></script>
<script src="libs/swipe.min.js"></script>      
<script src="dist/gdoc-powered-slider.min.js"></script>

<div id="slideshow"></div>

<script>
jQuery(function($) {
  $('#slideshow').slideshow('0AswaDV9q95oZdDZFSWpEZHlNRUlHWmVqa3JqalZsZXc');
});
</script>
```

## Writing your slideshow in a spreadsheet

The demo uses this spreadsheet https://docs.google.com/spreadsheet/pub?key=0AswaDV9q95oZdDZFSWpEZHlNRUlHWmVqa3JqalZsZXc&output=html

Each row is another slide in your slideshow. Each column is a different aspect of your slide you'd like to control. The columns we support are "title", "text", "top image", "bottom image", and "background image". I strongly recommend that you use only one of top, bottom, and background image.


## Examples
_(Coming soon)_

## License
Copyright (c) 2012 Ben Breedlove  
Licensed under the MIT, GPL licenses.

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [grunt](https://github.com/cowboy/grunt).

### Important notes
Please don't edit files in the `dist` subdirectory as they are generated via grunt. You'll find source code in the `src` subdirectory!

While grunt can run the included unit tests via PhantomJS, this shouldn't be considered a substitute for the real thing. Please be sure to test the `test/*.html` unit test file(s) in _actual_ browsers.

### Installing grunt
_This assumes you have [node.js](http://nodejs.org/) and [npm](http://npmjs.org/) installed already._

1. Test that grunt is installed globally by running `grunt --version` at the command-line.
1. If grunt isn't installed globally, run `npm install -g grunt` to install the latest version. _You may need to run `sudo npm install -g grunt`._
1. From the root directory of this project, run `npm install` to install the project's dependencies.

### Installing PhantomJS

In order for the qunit task to work properly, [PhantomJS](http://www.phantomjs.org/) must be installed and in the system PATH (if you can run "phantomjs" at the command line, this task should work).

Unfortunately, PhantomJS cannot be installed automatically via npm or grunt, so you need to install it yourself. There are a number of ways to install PhantomJS.

* [PhantomJS and Mac OS X](http://ariya.ofilabs.com/2012/02/phantomjs-and-mac-os-x.html)
* [PhantomJS Installation](http://code.google.com/p/phantomjs/wiki/Installation) (PhantomJS wiki)

Note that the `phantomjs` executable needs to be in the system `PATH` for grunt to see it.

* [How to set the path and environment variables in Windows](http://www.computerhope.com/issues/ch000549.htm)
* [Where does $PATH get set in OS X 10.6 Snow Leopard?](http://superuser.com/questions/69130/where-does-path-get-set-in-os-x-10-6-snow-leopard)
* [How do I change the PATH variable in Linux](https://www.google.com/search?q=How+do+I+change+the+PATH+variable+in+Linux)
