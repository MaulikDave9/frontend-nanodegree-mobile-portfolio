## Website Performance Optimization portfolio project ##

### Website: https://maulikdave9.github.io/frontend-nanodegree-mobile-portfolio/ ###

#### Use https://developers.google.com/speed/pagespeed/insights to find the pagespeed before and after making the changes: ####
Mobile: 93/100
Desktop: 94/100

#### From the main page (https://maulikdave9.github.io/frontend-nanodegree-mobile-portfolio/), please click " Cam's Pizzeria", open Developer tools to verify performance enhancements. ####

### Part 1:  PageSpeed Score ###
#### Optimizations in index.html for Critical Rendering Path changes to achieve score of at least 90 for Mobile and Desktop. ####

1. Remove importing/href web fonts
2. Inline css - style and print (non-blocking CSS)
3. "async" JavaScript 
4. 'Cam's Pizzaria' image was very large, resize/optimize.  
5. Downloaded images on local server instead of getting from web but that worsened pagespeed so put back image links.

### Part 2: Getting Rid of Jank ###
#### Optimizations in views/js/main.js for: ####
#### 1. Frame Rate: render with a consistent frame-rate at 60fps when scrolling. ####
#### 2. Computational Efficiency: Time to resize pizzas is less than 5 ms using the pizza size slider on the views/pizza.html page. ####


1. addEventListener: reduce the sliding pizzas when the page loads (from 200 to 24), declaring the elem variable (var elem;) in the initialization the for loop 
   to prevent from created everytime the loop is executed, 'movingPizzas' (DOM call) outside 'for' loop and define as local variable,  and change elem.basicLeft to elem.style.left for transform property.
2. updatePositions: change items[i].style.left to items[i].style.transform, and move 'phase' outside loop to prevent the DOM being explicitly touched in every
   iteration.
3. In function determineDx(elem, size), use document.getElementById(id) web API (faster) instead of document.querySelector(..).
4. In function changePizzaSizes(size) for loop was calculating each iteration what could be done out side loop, 
   define "document.querySelectorAll(".randomPizzaContainer")" as a var outside for loop and use getElementsByClassName() web API (faster)
   and bring calculations/calls that doesn't need to perform for all the iterations of for loop outside the loop!
5. Move 'pizzasDiv' that creates/appends all pizza on page load outside 'for' loop, so DOM call is made one time and not everytime for loop iterates.
