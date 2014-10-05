Responsive web design is a technique for building websites that work on mobile devices, tablets and desktop screen resolutions. It solves the problem of making the same code work across multiple screen resolutions. This post is an example to build a basic Responsive Blog Theme. This blog can be divided into the header and the body parts. We will set up the site's foundation, make the header and the navigation links.

First set up the basic HTML document structure. It includes the doctype, head and body.

```html
<!DOCTYPE html>
 <head>
  <!-- Meta info -->
 </head>
 <body>
  <!-- Page content -->
 </body>
```
`<header>` is a special tag in HTML5 for headers. It is a container that holds the elements we use to make the header.

Put an image and headline inside the `<header>` tag and a navigation bar. Use the `<ul>` and `<li>` tags for the navigation bar.

```html
<header>
 <img src="http://avireni.github.io/assets/avatar.png">
 <h1>Beena's Blog</h1>
 <ul>
  <li><a href="#">About Me</a></li>
  <li><a href="#">Writing</a></li>
  <li><a href="#">Work</a></li>
 </ul>
</header>
```
Add `Normalize.css` as a link,

```html
<link href="css/normalize.css" rel="stylesheet">
```
`Normalize.css` renders all elements more consistently and in line with modern standards. Our page will look the same, no matter what browser is used.

We need to align our header elements to the center and line up the list elements next to each other. Hence use `display` attribute and give it a value as `inline`. We can also achieve the look by styling the elements as `float: left;` , but `display: inline` is the correct way to do it.  

Every html element has a default value for display, either `Block` or `Inline`. Elements like headings, paragraphs etc display block by default. It means they stretch the whole width of the page and have line breaks before and after. Elements like `<a>` `<img>` display inline by default. They exist within the normal flow of the text they are contained within. They don't take the full width of the page and no line breaks either. 

I used the `article` tag to wrap the content on the page. It groups together multiple HTML elements that form single piece of content. Align it to the center of page.

There are some CSS tricks to make the web content adapt gracefully to different screen widths. `Media Query` is a technique that allows us to set CSS styles that only activate when the browser is a certain width.

```html
@media (max-width: 500px) {
	body {
		background: red;
		}
	li {
		display: block;
		padding: 5px;
		}
	}
```

Here, we are setting a condition, that the browser should be smaller than 500px, and when that condition is true the CSS inside this code block gets activated. So thats pretty much to it. We now have our responsive blog ready. You can find the [demo here](http://avireni.github.io/ResponsiveBlogTheme) and [source here](https://github.com/avireni/ResponsiveBlogTheme)
