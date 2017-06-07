## Website Performance Optimization portfolio project

#### Part 1: Optimizations in index.html (To achieve score of at least 90 for Mobile and Desktop)

Use https://developers.google.com/speed/pagespeed/insights to find the pagespeed before and after making the changes.
Changes that enabled the pagespeed 90:
Mobile: 91/100
Desktop: 92/100

(1) Remove importing/href web fonts
(2) Inline css - style and print (non-blocking CSS)
(3) "async" JavaScript 
(4) 'Cam's Pizzaria' image was very large, resize/optimize.  
(5) Download images on local server instead of getting from web as an experiment but that surprisingly didn't help 
    reduce the pagespeed.




#### Part 2: Optimizations in views/js/main.js for pizza.html.

