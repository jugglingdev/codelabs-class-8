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

The accordion project was pretty neat because the CSS carried as much weight as the JS to make it work.  In it, there are 3 simple questions that the user can click to make answers appear.  I added the functionality that only one answer can be open at a time, though it's possible to change that so you can have as many open as you'd like at a time.

In the CSS, I liked using `transform` to make the chevron icons rotate when opening and closing.  I also liked getting a little practice with `cubic-bezier` as a `transition` value to customize the timing of a transition.

I used an `open` class to style a list item with the answer showing.  In the JS, instead of adding and removing the `open` class with two separate functions to make the list items open and close, I used `toggle()`.

A neat little trick I used in this project was to `console.log(this)` to see what `this` refers to.  In `toggleAccordion()`, `this` referred to the `question` element, but I needed it to refer to the `li` element.  I used `this.parentNode` to do just that.



## Scrolling Progress

This nifty component features an indicator that fills up based on how much you have scrolled through a given article.  While simple, the logic behind it is neat.

3 variables - `windowHeight` (the height of the window), `fullHeight` (the height of the page including the parts hidden before scrolling), and `scrolled` (how many pixels the document is currently scrolled from the top of the viewport) - are used to calculate the `percentScrolled` and update the indicator.

In order to help the program run efficiently when working with larger pages, the `debounce()` function from the Lodash library is used to limit how often the indicator updates.  I used the default wait time of 15 milliseconds.



## Reflection

