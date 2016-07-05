# Day 2 Course Notes

### File system:

#### portfolio-site

* version1
  * index.html
  * css/style.css
  * img/ali.jpg

* version2
  * index.html
  * css/style.css
  * img/ images

### HTML Concepts covered

#### Comments:

```
<!-- I am a comment, ignored by the browser -->
<p>I am a paragraph displayed by the browser</p>
```

#### Tags:
```
<html>
<head>
<body>
<header>
<section>
<footer>
<div>
<p>
<img>
<a>
```

#### Classes:

In your HTML file:

```
<h1 class="tagline">Heading content</h1>
```

And then in your CSS:

```
h1.tagline {
  font-size: 120%;
}
```

or to target all HTML tags with a class of 'tagline', not just h1s:

```
.tagline {
  font-size: 120%;
}
```

#### Image Attributes

```
<img src="path/to/image.jpg" alt="Description of image">
```

#### Image optimisation

Images can be .jpg .gif .png and so on. Images need to be optimised for the web, as an image taken with an 8MP camera will have a huge filesize and will use up your user's data plan, as well as taking ages to download.

### CSS Concepts covered

#### Target an HTML tag and give it a list of styles:

```
p {
  color: blue;
  font-weight: bold;
}
```

#### Target a set of HTML elements using a class:

```
.profile-picture {
  width: 50%;
  display: block;
  margin: auto;
}
```

(The above will also centre an image)

#### Give an element breathing room

```
header {
  padding: 1rem;
}
```

#### Target multiple elements in one go

```
header, section, footer {
  padding: 1rem;
}
```

#### Centering images

Images are [actually a mixture of inline and block elements](http://stackoverflow.com/questions/2402761/is-img-element-block-level-or-inline-level) so they can be centred in two ways:

1. Using text-align: center; on an image's parent element

```
<section>
  <img src="../path/to/image.jpg">
</section>
```

```
section {
  text-align: center;
}
```

2. Setting the image's display property to block, and telling its margins to be equal on both sides:

```
img {
  display: block;
  margin: auto;
}
```

#### Using colour and transparency

We saw that you can specify color using rgb(redNumber, greenNumber, blueNumber). And that you can also use rgba(redNumber, greenNumber, blueNumber, alphaValue) to set a transparent color.

```
section {
  background: rgba(255,255,255,0.8);
}
```

The above will set the background color of section elements to be 80% white.

#### Working with background images

We also learnt how to work with background images.

```

body {
  background-image: url(../path/to/image.jpg);
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
}
```

### Further reading

[Have a read about 'ems' and 'rems'](https://codemyviews.com/blog/whats-the-deal-with-em-and-rem)

[And about Bootstrap](http://www.w3schools.com/bootstrap/)

[And GitHub](https://guides.github.com/activities/hello-world/)

[And also GitHub pages](https://pages.github.com/)







