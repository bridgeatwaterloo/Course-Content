# Day 3 Course Notes

### Making a centrally aligned, fixed position navigation

```
<nav>
    <ul>
        <li>
            <a href="index.html">Home</a>
        </li>
        <li>
            <a href="about.html">About</a>
        </li>
    </ul>
</nav>
```

Set the nav to be full-width and to have a background-color:

```
nav {
  width: 100%;
  background-color: black;
  position: fixed;
  bottom: 0rem;
}
```

We also set its position to fixed and its 'bottom' property to 0rem so it sits at the bottom of the page.

Next, target the unordered list and remove its default margin and padding, the bullet points, and set it to display its contents in the center:

```
nav ul {
    text-align: center;
    list-style: none;
    padding: 0;
    margin: 0;
}
```

Set the list items to display inline so that they appear on the same line:

```
nav ul li {
    display: inline;
}
```

Finally, we target our links, giving them some padding so users can always tap or click them.

```
nav ul li a {
    display: inline-block;
    padding: 1rem;
    text-decoration: none;
    background: black;
    color: white;
}
```




### Resources

* [Playto: Margins, Padding and the Box Model](https://learn.playto.io/html-css/lesson/9)
[Mozilla Developer Network (MDN): Box Model](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model)
* [CSS Selectors](http://www.w3schools.com/cssref/css_selectors.asp)
* [HTML5 Boilerplate](http://html5boilerplate.com)
* __Extensive__ 1 hour long [video](https://www.youtube.com/watch?v=gqOEoUR5RHg) explaining how to get started with Bootstrap v3.3.6 (4.0 currently in Alpha).
* [Initializr](http://www.initializr.com/) is a great way to create a HTML5 template.

### Further reading

* [Playto: Absolute, Relative and Fixed positioning](https://learn.playto.io/html-css/lesson/12)

### Inspiration

[You don't need JavaScript](https://github.com/NamPNQ/You-Dont-Need-Javascript)
