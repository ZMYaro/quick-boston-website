# <abbr title="Queer Inclusive Climbing Klub">QuICK</abbr> Boston Website

This is an attempted rebuild of the QuICK Boston Squarespace website as basic HTML.


## Setting up an instance

* You can clone/download this repository and just open `index.html` in any modern web browser.
* The social media icons may only work if you serve the site from a web server.
	- This is due to the way those icons are added (through an SVG `<use>`), which allows them to be recolored to match the text around them.
	- Any basic web server—e.g., Apache, Node's `http-server`, Python 2's `SimpleHTTPServer`, or Python 3's `http.server`.


## Page components

* Matching the design of the existing site, the page has a `<header id="page-header">` and full-width `<section>`s.
* Each section can have a background image set with an inline `background-image` style.  It can be given `class="dim-background"` or `class="lighten-background"` if necessary to keep text readable.
* The intro section has an `<h1>`; the headings of subsequent sections should be `<h2>`s, and then headings for list items within those sections should be `<h3>`s.
* A section can include a `<ul class="multi-column-list">`, which will arrange its child elements into rows when there is sufficient horizontal space.
	- The `#meet-up-list` and `#people-list` lists have additional styles specific to those lists.


## Accessibility

* Images that are necessary to understanding the page should have alt text (`<img src="[...]" alt="[...]" />`).
	- Alt text should be brief, in the active voice, and describe the contents of the image relevant to its context on the page.
	- Alt text _shouldn't_ include “A photograph of...”/“A drawing of...”/etc. unless that is relevant to the image's context on the page.
	- If an image needs a longer description, include a shorter description in the `alt="[...]"`, and then add `aria-description="[...]"` with the longer description.
* Images that _aren't_ necessary to understanding the page should have `alt=""` to indicate that.
* Other elements that aren't screen reader accessible and aren't necessary to using/understanding the page should have `aria-hidden="true"`.
	- This is currently used to hide the gym thumbnail links since the thumbnails themselves don't have image descriptions.


## Code style

* Follow [standard Git commit message guidelines](http://git-scm.com/book/ch5-2.html#Commit-Guidelines).
  - Commits messages should fit in the sentence, “If applied, this commit will \_\_\_\_.”
* Indent code with tabs, not spaces.
* CSS class and id names are in `kebab-case` (i.e. all lowercase with hyphens between words; _not_ `camelCase` or `snake_case`).
