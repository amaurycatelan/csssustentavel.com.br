---
layout: chapter
title: Files
section: Extras
permalink: /chapters/files/
description: What does a maintainable CSS file look like?
---

There are only a few things to consider in order to write a maintainable CSS file. But first, it's worth noting that these guides pertain to vanilla CSS. If you're using a CSS preprocessor, you can still take away the principles and apply them to the syntax of your chosen preprocessor.

## 1. Media Queries

Generally speaking, the screen should adapt to the content, not the other way around. With this in mind it could be that some modules don't require any breakpoints when others require five for example. 

Attempting to crow bar all screens in to say 3 predefined breakpoints is something that is unecessarily constraining to a design, ultimately degrading the User Experience.

In a site I worked on recently, the header had just one breakpoint based on the navigation being able to fit on one line or not. That breakpoint happened to be `500px`. Then below the header, there was a module that had a breakpoint of `650px` which is where the content needed a breakpoint to take into account the extra space available to it.

For these reasons, styles residing in breakpoints should be located in very close proximity to a style not wrapped by a breakpoint. See below for an example:

	.basket {}

	@media(min-width: 500px) {
		.basket {}
	}

	@media(min-width: 1000px) {
		.basket {}
	}

	.basket-heading {}

## States and modifiers

Just like media queries, states and modifiers should be located in close proximity to the element they pertain to:

	.basket {}

	.basket-isHidden {}

	.basket-heading {}

	.basket-heading-someModifier {}

## Comments

If you have multiple modules residing in a single file, then it's useful to split up these modules with an obvious well named comment:
	
	/********************************************
	* Basket
	********************************************/

	.basket {}

	.basket-heading {}

	/********************************************
	* Banana
	********************************************/

	.banana {}

	.banana-details {}