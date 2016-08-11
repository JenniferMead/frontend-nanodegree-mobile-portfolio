###Overview
This project was completed for Udacity's Front End Nanodegree Program. The goal of the project was to optimize the websites load time and animation speeds.


###Viewing the portfolio
Download the code by selecting 'Download ZIP'. Then simply open the frontend-nanodegree-mobile-portfolio folder, right click on index.html, and open in the browser of your choice.


###Optimizations Made to index.html
1. Used a web font loader to defer the loading of google fonts until AFTER other parts of the page have started to load. I also made it an asynchronous script.
2. Used a media query to prevent the print.css from render blocking
3. Changed script.css from an external file to internal css style sheet using a script tag and moving it over to the HTML
4. Compressed all images and reduced sizes where approprtiate.
5. Made a separate pizzaria image with a reduced size so that the index.html didn't need to reference the image in the views/images folder which was bigger than needed for the front page
6. Overall, improved the page speed insight score from around a 30/100 for mobile and desktop to a 98/100 for mobile and desktop!


###Optimizations made to views/js/main.js
1. Optimized the pizza resizing script 
  * I separated the changePizzaSizes function into two separate functions to prevent recalculating layout and then style. To do this I made a separate function called layout that calculates the layout and then returns the results to be used later by the changePizzaSizes function. 
  * I avoided accessing the DOM to get the randomPizzaContainer class  multiple times by accessing it outside of both functions and holding it variables.
2. Optimized the pizza scrolling script
3. 

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

### Customization with Bootstrap
The portfolio was built on Twitter's <a href="http://getbootstrap.com/">Bootstrap</a> framework. All custom styles are in `dist/css/portfolio.css` in the portfolio repo.

* <a href="http://getbootstrap.com/css/">Bootstrap's CSS Classes</a>
* <a href="http://getbootstrap.com/components/">Bootstrap's Components</a>
