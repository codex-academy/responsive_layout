# Responsive webpages

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

When using floats it is important to create a containing element and to clear the float using a clearfix on the containing element to prevent elements below the floated elements to be pulled up as well.

```css
.box {
	width: 25%;
	float: left;
}

.clearfix {
  overflow: auto;
  zoom: 1;
}
```

```html
<div class="boxes clearfix">
	<div class="box">
		this will float left and be next to a box
	</div>
	<div class="box">
		this will float left and be next to a box
	</div>
	<div class="box">
		this will float left and be next to a box
	</div>
</div>
<div class="under">
	This element will pull up if the boxed element don't clear the float using a clearfix.
</div>
```



### Flexbox

Flexbox is a newer way to create web page layouts. It's an easy way to split a page up into equal parts on an horizontal axis.

You can see from the examples below that using flexbox standard settings for horizontal layouts use less css than floats.

```css
.boxes {
	display: flex
}

.wider {
	flex : 2
}
```

```html
<div class="boxes">
	<div class="box">
		this will be next to a box and not below
	</div>
	<div class="box wider">
		this will be next to a box and not below. but twice wider than the other to box elements.
	</div>
	<div class="box">
		this will be next to a box and not below
	</div>
</div>
<div class="under">
	This element will pull up if the boxed element don't clear the float using a clearfix.
</div>
```

