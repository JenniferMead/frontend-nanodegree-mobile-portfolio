###Overview
This project was completed for Udacity's Front End Nanodegree Program. The goal of the project was to optimize the websites load time and animation speeds.


###Viewing the portfolio
Download the code by selecting 'Download ZIP'. Then simply open the frontend-nanodegree-mobile-portfolio folder, right click on index.html, and open in the browser of your choice.


###Optimizations made to index.html
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
  * I separated the for loop inside of the updatePositions function into two different for loops, one to calculate the var called phase (layout calculation), which I stored in an array called pizzaHolder, and the other to calculate the style. 
  * I separated out the var lengthHolder and phaseHolder from their for loops becuase those values don't change and don't need to be recalculated over and over again.
  * In the event listener at the bottom of the code I changed the number of pizzas being created from 200 to 35 becuase 200 pizzas is unessary and time consuming to create.
  * I moved declaring and defining the variable items outside of the updatePosition function becuase the DOM doesn't need to be queried for this every time you scroll. I declared the var items globally, then I defined it within the event listener so that the DOM is only queried once when the DOM content is loaded. I also changed querySelectorAll to getElementsByClass name when defining items becuase its faster.

### Resources
Udacity Front-End Web Developer Nanodegree
