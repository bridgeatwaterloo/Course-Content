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

  <!-- I am a comment, ignored by the browser -->
  <p>I am a paragraph displayed by the browser</p>

#### Tags:
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

#### Classes:

In your HTML file:

  <h1 class="tagline">Heading content</h1>

And then in your CSS:

  h1.tagline {
    font-size: 120%;
  }

or to target all HTML tags with a class of 'tagline', not just h1s:

  .tagline {
    font-size: 120%;
  }

#### Image Attributes

  <img src="path/to/image.jpg" alt="Description of image">

#### Image optimisation

Images can be .jpg .gif .png and so on. Images need to be optimised for the web, as an image taken with an 8MP camera will have a huge filesize and will use up your user's data plan, as well as taking ages to download.


