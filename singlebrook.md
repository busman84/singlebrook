singlebrook.md

# Getting Started

Since my file structure is already made for me in the starter code, my next step would be to fill in the index.html skeleton.

index.html
```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
</head>
<body>
	
</body>
</html>
```

Now that I have the skeleton html, I am going to change the title and add the link to my style.css style sheet.**Note that I am using the relative path**


index.html
```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Singlebrook Home</title>
	<link rel="stylesheet" href="css/style.css">
</head>
<body>
	
</body>
</html>
```
	- Quick tip: Make sure now that your style sheet is connected correctly by adding a back-ground color to the body and open your page.  If the background color is still white that it hasn't been connected yet!

style.css
```css
body{
	background-color: blue;
}
```

Our style sheet is connected! My next step is to now go ahead and take a look at the mock-up and try to break it down.  After looking at it, I have decided that I am going to use zurb foundation for my CSS framework, and therefore I must now go get the [CDN link from their webpage](http://foundation.zurb.com/sites/docs/installation.html).
Now that I have the CDN I am going to add it into our style.css.  Notice that I am putting this link above my already linked style.css. This is so that the styles I ultimately create will not get over ridden by any of zurb foundations styles.  

index.html
```html
<head>
	<meta charset="UTF-8">
	<title>Singlebrook Home</title>
	<link rel="stylesheet" href="https://cdn.jsdelivr.net/foundation/6.2.0/foundation.min.css">
	<link rel="stylesheet" href="css/style.css">
</head>
```

Okay, so not that  we are ready to go with zurb foundation, lets get down to business.

First think I notice is that we have a header on the page. So I am going to add in a header into the body of our index.html file.

index.html
```html
<body>
	<header>
		
	</header>
</body>
```

I have decided that I am going to give this header a class of row, and split it into four columns of 5-1-3-3.  Using the zurb foundation docs I have determined which classes to give to my divs to create the correct columns.

index.html
```html
<header class="row">
	<div class="columns large-5"></div>
	<div class="columns large-1"></div>
	<div class="columns large-3"></div>
	<div class="columns large-3"></div>
</header>
```
I have divided my sections up how I beleive they should be laid out so next lets add the content within.

	1. In the first div I see that there is an image to add
	2. In the second div I see that there appears to be a list
	3. In the third div I notice a paragraph that has a link at the end of it
	4. Finally, in the fourth div I notice some sort of form and button

I am also going to add a class 'turq' to my header and create a css rule that makes the background of the header the color code provided

index.html
```html
<header class="row turq">
		<div class="columns large-5">
			<img src="images/singlebrook_logo.png" alt="">
		</div>
		<div class="columns large-1">
			<ul>
				<li>Work</li>
				<li>Services</li>
				<li>Mission</li>
				<li>Team</li>
				<li>Blog</li>
				<li>Contact</li>
			</ul>
		</div>
		<div class="columns large-3">
			<p>We build web and mobile software with a mission of Technology for Change. <a href="#">Read more now</a></p>
		</div>
		<div class="columns large-3">
			<form action="post">
				<input type="text">
				<input type="submit">
			</form>
		</div>
	</header>
```

style.css
```css
.turq{
	background-color: #00d6dd;
}
```

If we look at the browser this is how our page looks right now.

[header](header.png) 

