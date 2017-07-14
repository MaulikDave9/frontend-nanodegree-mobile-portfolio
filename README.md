## Website Performance Optimization portfolio project ##

### Part 1:  ###

Use https://developers.google.com/speed/pagespeed/insights to find the pagespeed before and after making the changes.
Mobile: 93/100
Desktop: 94/100

#### Optimizations in index.html (To achieve score of at least 90 for Mobile and Desktop) for the pagespeed 90: ####

1. Remove importing/href web fonts
2. Inline css - style and print (non-blocking CSS)
3. "async" JavaScript 
4. 'Cam's Pizzaria' image was very large, resize/optimize.  
5. Downloaded images on local server instead of getting from web but that worsened pagespeed so put back image links.



### Part 2: Getting Rid of Jank ###

#### Optimizations in views/js/main.js for: ####

#### Frame Rate: render with a consistent frame-rate at 60fps when scrolling. ####

1. addEventListener: reduce the sliding pizzas when the page loads (from 200 to 24) 
   and change elem.basicLeft to elem.style.Left for transform property.
2. updatePositions: change items[i].style.left to items[i].style.transform.

#### Computational Efficiency: Time to resize pizzas is less than 5 ms using the pizza size slider on the views/pizza.html page. ####

1. Define "document.querySelectorAll(".randomPizzaContainer")" as a var outside for loop in function changePizzaSizes(size)
   and bring calculations that doesn't need to perform for all the iterations of for loop, outside the loop!

On Chrome browser: "Time to resize pizzas: 0.5299999999951979ms", on Mozilla browser working not so good.  Hope it's not code issue but browser issue.