<!DOCTYPE html>
# Responsive webpages</h1>

Responsive web pages respond to the available screen size and move the web page elements around to ensure a good user experience.

By combining Media Queries & Layout techniques you can create a responsive web page, that display elements below each other if the page is **narrow** and next to each other if the page is **wider**.
		
* [Media queries](href="media-query.html">) help to control which CSS is active based on the width of the screen.
* Using layout techniques such as [Floats] (layout.html) & [Flexbox](layout.flex.html)elements can be moved around on the web page.

## Media Queries

```css

/* CSS that will be active if the screen is less than 600 pixels or if the screen is wider id it's not over ridden in a media query. */

@media and screen and (min-width : 600px) {
	/* css that will be active wider than 600 pixel screen width */
}

@media and screen and (min-width : 1000px) {
	/* css that will be active wider than 1000 pixel screen width */
}

```

## Layout techniques

There are various different ways to get elements in an HTML page to move from their default positions.

### Floats

Floats are one of the oldest and most trusted ways to layout web pages with. But it is also quite quirky. And one can easily create a mess using floats if you are not carefull.

When using floats it is important to created containing elements and the clear the float using a clearfix to prevent elemts below the floated elements to be pulled up as well.

```css

.box {
	width: 25%;
	float: left;
}

.clearfix {
	
}

```

### Flexbox

Flexbox is a newer way to create web page layouts. It's an easy way to split a page up into equal parts on an horizontal axis.

```css
.boxes {
	display: flex
}
```

