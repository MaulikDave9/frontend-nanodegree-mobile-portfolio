## Website Performance Optimization portfolio project ##

### Part 1: Optimizations in index.html (To achieve score of at least 90 for Mobile and Desktop) ###

Use https://developers.google.com/speed/pagespeed/insights to find the pagespeed before and after making the changes.
Mobile: 93/100
Desktop: 94/100

#### Changes that enabled the pagespeed 90: ####

1. Remove importing/href web fonts
2. Inline css - style and print (non-blocking CSS)
3. "async" JavaScript 
4. 'Cam's Pizzaria' image was very large, resize/optimize.  
5. Downloaded images on local server instead of getting from web but that worsened pagespeed so put back image links.



### Part 2: Optimizations in views/js/main.js for pizza.html ###

1. Reduces the sliding pizzas when the page loads (from 200 to 24).
2. Change items[i].style.left to items[i].style.transform in function updatePositions() 
3. Define "document.querySelectorAll(".randomPizzaContainer")" as a var outside for loop in function changePizzaSizes(size)



