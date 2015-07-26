## Website Performance Optimization portfolio project

My challenge was to optimize this online portfolio for speed! In particular, to optimize the critical rendering path and make this page render as quickly as possible by applying the techniques I picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

### Instructions to Run

1. Clone the repository from Github.

2. Point your browser to index.html.

### Optimizations

####Part 1: Optimize PageSpeed Insights score for index.html

Here are the optimizations I made to index.html:

- Optimized images
- Inlined styles
- Added media="print" to ignore print styles unless printing
- Moved JavaScript references to bottom of body
- Switched to use async Web Font loader

This page now renders with a PageSpeed Score of 95.

####Part 2: Optimize Frames per Second in pizza.html

To optimize the framerate of pizza.html, the following changes were made to main.js:

- Pre-constructed array of movers on DOMContentLoaded instead of on every scroll
- Used document.getElementsByClassName() instead of the slower document.querySelectorAll()
- Pre-calculated the 5 scroll phases to avoid calculating for each mover in the loop
- Avoided moving off-screen pizzas, reduced number from 200 to 32

On my computer, 10 frames render in well under 1ms.