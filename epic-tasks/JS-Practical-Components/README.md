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

## Coding Playground

## Stopwatch

## Accordion

## Scrolling Progress

## Reflection

