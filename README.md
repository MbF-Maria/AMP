AMP Documentation : https://www.ampproject.org/docs/

Basic Example of AMP : https://ampbyexample.com/introduction/hello_world/

Rules of AMP :

- You may include 1 <style> tag in the <head> of the DOM. You must append amp-custom to the <style> tag like this: <style amp-custom>your style rules here</style>
- You may not alter the margin property on the body element.
- You may not load an external stylesheet or import one via @import
- You may not add style attributes to elements.
- You may not use the !important qualifier.
- You may never use any of the following properties:
	behavior:
	overflow: scroll
	overflow: auto
	transition:
	filter
	animation
	-moz-binding
- You may use the following selectors:
	.class e.g. .row
	#id e.g. #sidebar
	tag-name e.g. section
	selector, selector e.g. .row, .clearfix or #sidebar, #main-body, article
	media queries e.g. @media (max-width:48em){}
- You may use the following pseudo-selectors:
	:hover
	:active
	:visited
- You may not use any input elements with the exception of button (as these are used to interact with AMP Web Components).
- You are obliged to avoid using class names prefixed with -amp or -amp- to avoid conflicting with AMP components. You can override the styles of these components if you wish.
- Your style rules must not exceed 50KB.
- You may acquire font assets either through a whitelisted font vendor (... Google Fonts) or by fetching the font through @font-face via HTTP/HTTPS — i.e. not via data: or -JavaScript plugin (since JS is banned).
	
Given solution to Use External CSS
  JADE :
  <style amp-custom>
  	{% include "/assets/css/main.min.css" %}
  </style>
  PHP :
  <style amp-custom>
  	<?php include '/assets/css/main.min.css'; ?>
  </style>

** Important : Once you complete Design using AMP. You have to validate code by following steps in below link
https://www.ampproject.org/docs/fundamentals/validate
	
