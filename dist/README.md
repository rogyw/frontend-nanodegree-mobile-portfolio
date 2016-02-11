## Website Performance Optimization portfolio project

This repository contains Roger Woodroofe's completed Project 4 for the Udacity Front End Nanodegree.

The project challenge was to optimize the provided online portfolio for speed. In particular, to optimize the critical rendering path and make the index.html page render as quickly as possible by applying the techniques picked up in the [Udacity Critical Rendering Path course](https://www.udacity.com/course/ud884).

In addition, Roger took the oportunity to learn and practice web tooling and automation through the use of gulp.js automation configuration.

### Getting started

####Part 1: Optimize PageSpeed Insights score for index.html

To view the live version of this project:

1. Open a browser and visit http://rogyw.navevent.co.nz/frontend-nanodegree-mobile-portfolio/

1. To view the results in Google PageSpeed insights, open a browser and visit https://developers.google.com/speed/pagespeed/insights/?url=http%3A%2F%2Frogyw.navevent.co.nz%2Ffrontend-nanodegree-mobile-portfolio%2F

Please refer to [Forum Post](https://discussions.udacity.com/t/optimized-portfolios-all-cohorts/949/14?u=rogyw) for steps taken to optimize index.html.

For additional information, you can also view the changes made by Rogyw in the [Github Repository log](https://github.com/rogyw/frontend-nanodegree-mobile-portfolio/commits/master).

On completion, and prior to submission, gulp.js automation configuration file gulpfile.js was added to assist with optimisations and gh-pages deployment.

##### Using Gulp build tool with this project

1. Fork the [repository](https://github.com/rogyw/frontend-nanodegree-mobile-portfolio.git) on GitHub.
1. Use git to copy/clone your new repository to your local system.
1. Install [npm](https://docs.npmjs.com/getting-started/installing-node) if not already in use.
1. Install [gulp.js](http://gulpjs.com/) if not already in use.
1. Install all gulp packages used by project.
``` npm install --save-dev gulp-cssnano gulp-autoprefixer gulp-gh-pages gulp-uglify gulp-imagemin gulp-htmlmin run-sequence del```
1. Open your local console and change the current directory to the project root folder (and location of gulpfile.js). The subfolder `dist` contains the automatically generated optimised files.
1. To refresh the contents of `dist` folder use `gulp rebuild`.  the rebuild will delete the old dist folder and rebuild based on current source files.
1. To deploy the contents of `dist` folder to your live `gh-pages` for the repostitory on Github use `gulp deploy`
1. Test it worked!

####Part 2: Optimize Frames per Second in pizza.html

views/pizza.html was optimized by modifying views/js/main.js until the frames per second rate is 60 fps or higher. Instructive comments were provided in main.js.

##### Javascript modifications made to views/js/main.js
Roger made the following changes:

1. Changed code loops to remove instances of "Forced Synchronous Layout" by batching DOM read operations and then batching style changes - Avoids thrashing.
1. Simplified code to reduce complexity of calculations.
1. Changed the method of selecting elements in DOM from querySelectorAll() to getElementsByClassName().
1. Reduced number of sliding pizza's from 200 down to  based on anticipated maximum page resolution
1. Moved sliding pizzas to own layer in CSS
1. added comments to code and updated README

### Provided Reference Links: Optimization Tips and Tricks
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
## Contacts
Udacity - see [website](https://www.udacity.com/)

Roger Woodroofe, through [GitHub](https://github.com/rogyw) or email [rogyw@yahoo.co.nz](mailto:rogyw@yahoo.co.nz)
