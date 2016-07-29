## Website Performance Optimization portfolio project


For the first part, open up the index.html file in your browser. Use the Pagespeed Insights at https://developers.google.com/speed/pagespeed/insights/ to see suggestions to help index.html perform at 90+ Pagespeed. 

I optimized the index.html file to perform at a Pagespeed of 95+. I took the CSS from style.css and inlined it into the index.html file. I also removed the Google font stylesheet as it is unnecessary. I then added the media="print" rule to the print.css file link. Last but not least, I added the async tag to the Google analytics script link and also to the perfmatters.js script link. 

For the second part, open up the pizza.html file in your browser. Use the Chrome DevTools in your browser as well as the helpful comments in the main.js file to optimize for a 60 frames per second result. Most of the modifications will need to be made in the main.js. You can also modify the style.CSS for an additional boost. 

I optimized the main.js and the style.css files to reach 60 frames per second. For the CSS file, I added the "backface-visibility: hidden" and "will-change: transform" attributes to the mover class. In the main.js, I started by refactoring the changePizzaSizes function. First I changed the QuerySelectorAll to getElementsByClassName and also removed the dx variable as it was unnecessary. I then added the newWidth variables to the switch cases followed by breaks. 

For the updatePositions function in main.js, I took the document.body.scrollTop out of the for loop. Also, changed the QuerySelectorAll to getElementsByClassName for efficient lookup and assigned items.length to the cache variable. Created a new Array and pushed the values from the first for loop into the array. I then changed the style.Basicleft in the second for loop to use the transform translateX to re-position the pizza images. 
