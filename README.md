# slick-headstart
Slick - Headstart

Based on 'Slick' at https://github.com/kenwheeler/slick and http://kenwheeler.github.io/slick/

... the last carousel you'll ever need

- Fully responsive. Scales with its container.

- Separate settings per breakpoint

- Uses CSS3 when available. Fully functional when not.

- Swipe enabled. Or disabled, if you prefer.

- Desktop mouse dragging

- Infinite looping.

- Fully accessible with arrow key navigation

- Add, remove, filter & unfilter slides

- Autoplay, dots, arrows, callbacks, etc...

#Getting Started

Set up your HTML markup.

```javascript
<div class="your-class">
  <div>your content</div>
  <div>your content</div>
  <div>your content</div>
</div>
```

#Move the /slick folder into your project

#Add slick.css in your <head>

```javascript
<link rel="stylesheet" type="text/css" href="slick/slick.css"/>
// Add the new slick-theme.css if you want the default styling
<link rel="stylesheet" type="text/css" href="slick/slick-theme.css"/>
```

#Add slick.js before your closing <body> tag, after jQuery (requires jQuery 1.7 +)

```javascript
<script type="text/javascript" src="//code.jquery.com/jquery-1.11.0.min.js"></script>
<script type="text/javascript" src="//code.jquery.com/jquery-migrate-1.2.1.min.js"></script>
<script type="text/javascript" src="slick/slick.min.js"></script>
```

#Initialize your slider in your script file or an inline script tag

```javascript
$(document).ready(function(){
  $('.your-class').slick({
    setting-name: setting-value
  });
});
```

#When complete, your HTML should look something like:

```javascript
<html>
  <head>
  <title>My Now Amazing Webpage</title>
  <link rel="stylesheet" type="text/css" href="slick/slick.css"/>
  <link rel="stylesheet" type="text/css" href="slick/slick-theme.css"/>
  </head>
  <body>

  <div class="your-class">
    <div>your content</div>
    <div>your content</div>
    <div>your content</div>
  </div>

  <script type="text/javascript" src="//code.jquery.com/jquery-1.11.0.min.js"></script>
  <script type="text/javascript" src="//code.jquery.com/jquery-migrate-1.2.1.min.js"></script>
  <script type="text/javascript" src="slick/slick.min.js"></script>

  <script type="text/javascript">
    $(document).ready(function(){
      $('.your-class').slick({
        setting-name: setting-value
      });
    });
  </script>

  </body>
</html>
```

***NOTE***: I highly recommend putting your initialization script in an external JS file.

#Settings

See http://kenwheeler.github.io/slick/

#Events

In slick 1.4, callback methods have been deprecated and replaced with events. Use them as shown below:

```javascript
// On swipe event
$('.your-element').on('swipe', function(event, slick, direction){
  console.log(direction);
  // left
});

// On edge hit
$('.your-element').on('edge', function(event, slick, direction){
  console.log('edge was hit')
});

// On before slide change
$('.your-element').on('beforeChange', function(event, slick, currentSlide, nextSlide){
  console.log(nextSlide);
});
```

See for more about events http://kenwheeler.github.io/slick/

#Methods

Methods are called on slick instances through the slick method itself in version 1.4, see below:

```javascript
// Add a slide
$('.your-element').slick('slickAdd',"<div></div>");

// Get the current slide
var currentSlide = $('.your-element').slick('slickCurrentSlide');
```

This new syntax allows you to call any internal slick method as well:

```javascript
// Manually refresh positioning of slick
$('.your-element').slick('setPosition');
```

See for more about methods http://kenwheeler.github.io/slick/

#Wordpress

Go Get It

(Download Now)[https://github.com/kenwheeler/slick/archive/1.6.0.zip]

(View On Github)[https://github.com/kenwheeler/slick/]

#Package Managers

# Bower

```javascript
bower install --save slick-carousel
```

# NPM

```javascript
npm install slick-carousel
```
