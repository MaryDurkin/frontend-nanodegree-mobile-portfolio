##Mary Walsh FEND Website Performance Optimization portfolio project

### Note for Susan, my Udacity Coach

Hi, thanks for reading this and helping me figure out my project.
I think I am fine on the first part of the project as I get good page speed scores on both modbile and dekstop.
(Actually, I have some nasty minified CSS inlined into the HTML, so it would not make pleasant viewing -
I'll fix it before I submit the project).

So I have two basic questions:

The first involves the frames per second for resizing the pizzas. I made the following optimizations:

* Resized the pizza.png and pizzeria.jpg
* Reduced the number of scrolling pizzas elements created to just those that will be displayed on the screen
* Replace selectQueryAll/selectQuery requests with getElementBy....
* Replaced style.left = with style.transform = "translateX..... when moving the pizzas
* Opimized loops in updatePositions() and changePizzaSizes() to
	- take all non iterative code out of the loop
	- minimize the number of caluclations like Math.sin
	- reduce DOM elemect lookups
* revoved (actually commented out) code that is no longer used, such as basic left.

The Timing API code now logs the "Average time to generate the lst 10 frames" at around  0.35ms
which would appear to be fast enough but the timeline still looks a little wonky. No forced reflow but I am unsure if I am making the required fps and am getting some red triangles on the gray line about 'Main thread'

The rezise pizza function is consistantly coming in at well under the 5ms allowance, so I am ok on this (I think?)

The second thing I need to do is to figure out how to use either grunt or gulp (or both?) to do the minifications and image resizing. until now I used photoshop for the images, and online tools for the minification.
I'll be looking at both before the appointment tomorrow, but may have questions and would appreciate any pointers.

Thanks again



