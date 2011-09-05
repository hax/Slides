# HTML5 Slides framework #

Just a simple slides framework built on HTML5 technologies

### How to apply this framework ###

* Write your slides document
	
	* using HTML5 structure as usual
	* But remember each section/header/footer element will be treat as one slide
	* Currently nest sections are not support well, improvement in plan

* Add these codes to your head of document:
	
		// change /Slides to your path
		// or http://raw.github.com/hax/Slides/master/src/ if you just want to use the latest version
		<link rel="stylesheet" href="/Slides/src/common.css">
		<link rel="stylesheet" media="projection, screen and (min-width: 780px)" href="/Slides/src/projection.css">
		<link rel="alternate stylesheet" title="slides" href="/Slides/src/play.css">
		<script src="/Slides/src/app.js"></script>

* Play slides

	* Press F11 (or any key which switch to fullscreen mode in your browser) to start/stop playing slides
	* In playing mode, press right arrow / pagedown to next slide and left arrow /pageup to previous slide
	* Browser back/forward button also works

### Browser Compatibility ###

This is a very new framework which only be tested under recent Chrome/Firefox, 
but it should work on any HTML5 browser.


HTML5 API this framework used:

* document.querySelectorAll

* Element.classList (compatibility patch in plan)

* popstate event (I plan to add compatibility patch for old browsers which not support popstate event in near future)

* window.fullScreen / fullscreenchange event (Mozilla-only API but a compatibility patch included)

* document.enableStyleSheetsForSet (CSSOM API, compatibility patch included though the implementation is not correct as spec)


CSS features this framework used:

* media query (min-width)

* css3 animation (WebKit extension, so u may not see animation in non-WebKit browsers)

	
Note: In general, all compatibility patches will be factor out and move to another project https://github.com/hax/homemade-html5 in the future