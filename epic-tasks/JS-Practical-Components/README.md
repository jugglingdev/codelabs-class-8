# Mastering Practical JavaScript: From DOM Interactions to Building Components

This series documents practical applications of the JavaScript concepts related to the DOM.  

## Pricing Calculator

In this project, I made a simple pricing calculator using form inputs for price and quantity.  Once the HTML was ready, I used JavaScript to grab the elements, add event listeners, and write functions that would execute upon interaction with the elements.  As the price and quantity are adjusted, the total cost changes.



## Button Playground

This was a fun little project that combined simple HTML, CSS, and JavaScript to make buttons that run away from the mouse upon hover.  Once again, after the elements were styled and ready, I grabbed them in the JavaScript and added event listeners and a function to randomize their positions on `mouseenter`.  

The randomized positioning was done with `Math.random()` multiplied by the height or width of this window (minus the button size).  What I liked about this calculation is there are two options to refer to the button size: 

1. Pass in `e` and use `e.target` to refer to the current button
2. Use `this` to refer to the current button

In past projects I've used `e` a lot, so it was neat to apply `this` here.



## Stopwatch

In this project, I whipped up a simple stopwatch that includes start, stop, and reset buttons that operate a timer.

One concept that I enjoyed about this project was the `pad()` function which makes sure that the seconds and minutes always have two digits each.  So, instead of showing `0:0`, `0:1`, etc., the timer would show `00:00`, `00:01`, etc.

Another concept that was helpful was the use of the `isRunning` boolean to return the start and stop functions so that multiple timers wouldn't be incrementing in the background.

I also appreciated that the `setInterval()` function was separated from `incrementTimer()` in order to keep the code clean and keep track of `interval` when calling `clearInterval(interval)` to stop the timer.  I'm a fan of small, easy-to-read functions.

Finally, I liked seeing an example of using JS `data-` attributes to grab an element.  If I were doing this on my own, I would have add an ID, so it was nice to see this alternative when you want to create custom attributes with JS.



## Accordion

## Scrolling Progress

## Reflection

