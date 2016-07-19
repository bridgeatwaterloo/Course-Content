## David Sprint 2

*[Trello Board](https://trello.com/b/8UZCBYz3/david-sprint-2)
*[Github Repo](https://github.com/bridgeatwaterloo/david-javascript-intro)

## HTML/CSS concepts:

### Working with Bootstrap

Yesterday we linked to Bootstrap using MaxCDN

Today the project template includes Bootstrap, and links to it using a relative path:

```
<link rel="stylesheet" href="bootstrap4/dist/css/bootstrap.css">
```

The HTML markup makes use of different Bootstrap components, including a nav, cards and buttons.

### Order matters

Bootstrap's JavaScript has a hard dependency on jQuery. This means it won't work without jQuery. The browser needs to have read jQuery before it reads the Bootstrap JavaScript file, otherwise it will complain in the console. Scripts therefore need to be in the following order:

```
<script src="path/to/jquery.js"></script>
<script src="path/to/bootstrap.js"></script>
```

### Classes recap

Each section element on the page (there are four of them) has a class of view:

```
<section class="view">...</section>
```

This means we can target all of them together from either our CSS or our JavaScript.

In order to target a specific view, we also give them their own unique class names:

```
<section class="view view-checkin">...</section>
<section class="view view-set-username">...</section>
<section class="view view-question">...</section>
<section class="view view-default">...</section>
```

You can have multiple class names in quotes, separated by spaces.

## JavaScript concepts:

### Variables and functions

We started by recapping our knowledge of variables and functions:

```
// JavaScript recap
var username = prompt("What is your name?");
alert("Hello there " + username);
```

In the above code, we declare a variable called username and assign the returned value of the prompt function to it.

We then use the JavaScript alert function to popup a greeting message

### Commenting out code

```
// JavaScript recap. Below code commented out
// var username = prompt("What is your name?");
// alert("Hello there " + username);
```

Putting code in comments means you can still see it, it just won't run in the browser

### jQuery

#### Selecting Elements

In CSS you can target elements using a selector like so:

```
.view {
  background: white;
  border: 1px solid grey;
}

.view-checkin {
  border: 1px solid green;
}
```

To target a series of elements in JavaScript, you would do the following:

```
var elements = document.getElementsByClassName('view');

```

This returns "an array-like object" of elements. So, elements[0] will equal the first section.view, elements[1] the second, and so on.

To hide all the elements, you would have to loop through this array, and set each element's display property to 'none'

```
for (var i = 0; i < elements.length; i++) {
  elements[i].style.display = 'none';
}

```

jQuery simplifies this clunky behaviour. It makes targeting elements work more like CSS:

```
$('.view')
```

Will return all elements.

To hide them all, we can use a special jQuery function (or method) called hide() which will hide all the elements returned by $('.view'):


```
$('.view').hide();
```

Similarly, we can get just one element by using the same syntax:

```
$('.view-checkin')
```

Will return just the section.view-checkin

And we can then run any jQuery method on it:

```
$('.view-checkin').show();
```

Try changing this to jQuery's fadeIn()

```
$('.view-checkin').fadeIn();
```

#### Events

jQuery can listen to events and trigger functions in response to them.

If we have a button with a class of submit-checkin

e.g.

```
<button class="btn btn-positive submit-checkin">Checkin</button>
```

We can target this and then listen to the click event on it:

```
$('.submit-checkin').on('click', processCheckin);

function processCheckin(event) {
  alert('button clicked!');
}
```

We are passing jQuery's on function two arguments:

1. The name of the event we want to listen to
2. The name of the function to run when that event happens








