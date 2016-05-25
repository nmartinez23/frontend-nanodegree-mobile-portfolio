## Website Performance Optimization portfolio project


1. For the first part, open up the index.html file in your browser. Use the Pagespeed Insights at https://developers.google.com/speed/pagespeed/insights/ to see suggestions to help index.html perform at 90+ Pagespeed. 

I optimized the index.html file to perform at a Pagespeed of 95+. I took the CSS from style.css and inlined it into the index.html file. I also removed the Google font stylesheet as it is unnecessary. I then added the media="print" rule to the print.css file link. Last but not least, I added the async tag to the Google analytics script link and also to the perfmatters.js script link. 

2. For the second part, open up the pizza.html file in your browser. Use the Chrome DevTools in your browser as well as the helpful comments in the main.js file to optimize for a 60 frames per second result. Most of the modifications will need to be made in the main.js. You can also modify the style.CSS for an additional boost. 

I optimized the main.js and the style.css files to reach 60 frames per second. For the CSS file, I added the "backface-visibility: hidden" and "will-change: transform" attributes to the mover class. In the main.js, I started by refactoring the changePizzaSizes function. First I changed the QuerySelectorAll to getElementsByClassName and also removed the dx variable as it was unnecessary. I then added the newWidth variables to the switch cases followed by breaks. 

For the updatePositions function in main.js, I took the document.body.scrollTop out of the for loop. Also, changed the QuerySelectorAll to getElementsByClassName for efficient lookup and assigned items.length to the cache variable. Created a new Array and pushed the values from the first for loop into the array. I then changed the style.Basicleft in the second for loop to use the transform translateX to re-position the pizza images. 

Want to give it a shot? Follow the instructions below if you want a challenging project!



Your challenge, if you wish to accept it (and we sure hope you will), is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

To get started, check out the repository, inspect the code,

### Getting started

####Part 1: Optimize PageSpeed Insights score for index.html

Some useful tips to help you get started:

1. Check out the repository
1. To inspect the site on your phone, you can run a local server

  ```bash
  $> cd /path/to/your-project-folder
  $> python -m SimpleHTTPServer 8080
  ```

1. Open a browser and visit localhost:8080
1. Download and install [ngrok](https://ngrok.com/) to make your local server accessible remotely.

  ``` bash
  $> cd /path/to/your-project-folder
  $> ngrok http 8080
  ```

1. Copy the public URL ngrok gives you and try running it through PageSpeed Insights! Optional: [More on integrating ngrok, Grunt and PageSpeed.](http://www.jamescryer.com/2014/06/12/grunt-pagespeed-and-ngrok-locally-testing/)

Profile, optimize, measure... and then lather, rinse, and repeat. Good luck!

####Part 2: Optimize Frames per Second in pizza.html

To optimize views/pizza.html, you will need to modify views/js/main.js until your frames per second rate is 60 fps or higher. You will find instructive comments in main.js. 

You might find the FPS Counter/HUD Display useful in Chrome developer tools described here: [Chrome Dev Tools tips-and-tricks](https://developer.chrome.com/devtools/docs/tips-and-tricks).

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
