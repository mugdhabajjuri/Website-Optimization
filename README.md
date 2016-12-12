# Website-Optimization
## Description
This is one of my project as a part of **udacity front end nano degree** program. You can find more about udacity and its courses [here] (https://in.udacity.com/). This project is about improving the speed to load the page and rendering an existing given portfolio site and also removing the jank. We can measure the speed of this site using chrome dev tools and perform optimisations required to improve page speed. The page speed can be known using the website [page speed insights](https://developers.google.com/speed/pagespeed/insights/)

## steps to follow

* Clone or download the repo.
* Use Google PageSpeed Insights to check the Google PageSeed score of the homepage.

## changes to optimize pizza.html in views/js/main.js 

1. In the changePizzaSizes function change the element selection by using getElementsByClassName() through class name rather than querySelectorAll and also added the elements to an array of pizzaElements.
2. The computations of the dx and newvalue variables are done outside of the for loop as it isn't required to recompute them in the loop.
3. In the updatePositions function changed the mover element selection by using class name rather than querySelectorAll.
4. As there are only 5 unique phases of the moving pizzas, I moved the phase calculation into its own for loop.
5. Moved the declaration of the pizzaDivs variable outside of the for loop, because it isn't needed to iterarte in the loop.
6. Changed the querySelector call for selecting movingPizzas1 element to getElementById, saved it to a local variable called movingPizzas, moved it outside of the for loop, and referenced the movingPizzas variable inside the loop.

## Optimizations to views/css/style.css

* Added backface-visibility: hidden; to the .mover class, to move each animated pizza to its own composite layer.

## Optimizations to index.html

* Inlined the styles.css to avoid render blocking.
* optimized the images to reduce the page load time.
* used aync for javascript to avoid render blocking.
