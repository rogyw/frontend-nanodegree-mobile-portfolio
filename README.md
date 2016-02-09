## Website Performance Optimization portfolio project

This repository contains Roger Woodroofe's completed Project 4 for the Udacity Front End Nanodegree.
The challenge was to optimize the provided online portfolio for speed. In particular, to optimize the critical rendering path and make the index.html page render as quickly as possible by applying the techniques picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

### Getting started

####Part 1: Optimize PageSpeed Insights score for index.html

To view the live version of this project:

1. Open a browser and visit http://rogyw.navevent.co.nz/frontend-nanodegree-mobile-portfolio/

1. To view the results in Google PageSpeed insights, open a browser and visit https://developers.google.com/speed/pagespeed/insights/?url=http%3A%2F%2Frogyw.navevent.co.nz%2Ffrontend-nanodegree-mobile-portfolio%2F

Please refer to [Forum Post](https://discussions.udacity.com/t/optimized-portfolios-all-cohorts/949/14?u=rogyw) for steps taken.
For additional information, you can check the changes made by Rogyw in the [Github Repository log](https://github.com/rogyw/frontend-nanodegree-mobile-portfolio/commits/master)

####Part 2: Optimize Frames per Second in pizza.html

views/pizza.html was optimized by modifying views/js/main.js until the frames per second rate is 60 fps or higher. Instructive comments were provided in main.js.

##### Javascript modifications to views/js/main.js
1. Removed Forced Synchronous Layout in javascript loops by batching reads and then batching style changes.
1. Simplified code to reduce complexity of calculations
1. Changed the method of selecting elements in DOM from querySelectorAll() to getElementsByClassName()
1. Reduced number of sliding pizza's based on anticipated maximum page resolution
1. Moved sliding pizzas to own layer in CSS
1. added comments to code





### Optimization Tips and Tricks
* [Optimizing Performance](https://developers.google.com/web/fundamentals/performance/ "web performance")
* [Analyzing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/analyzing-crp.html "analyzing crp")
* [Optimizing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/optimizing-critical-rendering-path.html "optimize the crp!")
* [Avoiding Rendering Blocking CSS](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-blocking-css.html "render blocking css")
* [Optimizing JavaScript](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/adding-interactivity-with-javascript.html "javascript")
* [Measuring with Navigation Timing](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/measure-crp.html "nav timing api"). We didn't cover the Navigation Timing API in the first two lessons but it's an incredibly useful tool for automated page profiling. I highly recommend reading.
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/eliminate-downloads.html">The fewer the downloads, the better</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer.html">Reduce the size of text</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/image-optimization.html">Optimize images</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/http-caching.html">HTTP caching</a>
* the FPS Counter/HUD Display may be useful in Chrome developer tools as described here: [Chrome Dev Tools tips-and-tricks](https://developer.chrome.com/devtools/docs/tips-and-tricks).

### Customization with Bootstrap
The portfolio was built on Twitter's <a href="http://getbootstrap.com/">Bootstrap</a> framework. All custom styles are in `dist/css/portfolio.css` in the portfolio repo.

* <a href="http://getbootstrap.com/css/">Bootstrap's CSS Classes</a>
* <a href="http://getbootstrap.com/components/">Bootstrap's Components</a>

