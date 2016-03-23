## Mary Walsh  - FEND - P4

### Website Performance Optimization Portfolio

There are src and dist folders containing source and production code. The dist folder can be found at the gh-pages version of the repository, [here](http://marydurkin.github.io/frontend-nanodegree-mobile-portfolio/)

(If you would like to rebuild the dist files, download the repository and run the grunt command in the terminal).

Here is a summary of the changes I made:

* In index.html, I inlined the the contents from style.css and attached an async tag to the js files
* Used a smaller version of pizzeria.js as the original one was huge.
* Used grunt to minimize the jpeg images and minify/uglify the css/html/js

These changes resulted in page speed insights scores of: 95-speed 100-UExp (mobile) and 97 (desktop)

* In Cam's pizzeria I rewrote a lot of main.js, in particular the following improvements:
	- optimized the loops
	- used more efficient dom lookups (getElementBy.....instead of querySelector).
	- used translateX to move the moving pizzas (and reduce layout costs)
	- changed the number of (moving) pizzas displayed to just those that will fit on the screen.
* Used a smaller version (but not as small as the index.html version) of pizzeria.jpg
* In style.css I added a backface-visibility style to the .mover class - this forces the moving pizzas onto a separate layer (thanks to my previous reviewer for this suggestion!)
* Used grunt to resize images & minify/uglify the html/css/js and produce the dist code

These changes resulted in the following measurements:
* the 'average time to generate last 10 frames' when scrolling is between 0.3 and 0.47ms, with no forced reflow 	visible in the devtools timeline.
* the 'Time to resize pizzas:' measurement comes between 1.16 and 2.33ms

## Thank You!

### Mary Walsh FEND - P4






