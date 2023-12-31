# Mastering Practical JavaScript: From DOM Interactions to Building Components

This series documents practical applications of JavaScript concepts related to the DOM.  The projects listed below are included in Chris Sev's [Getting Started with JavaScript](https://chrissev.gumroad.com/l/getting-started-with-javascript/) course as a part of the [Codefi CodeLabs](https://www.codelabsdash.com/) bootcamp curriculum.

## Table of Contents
- [Mastering Practical JavaScript: From DOM Interactions to Building Components](#mastering-practical-javascript-from-dom-interactions-to-building-components)
  - [Table of Contents](#table-of-contents)
  - [The Projects](#the-projects)
    - [Pricing Calculator](#pricing-calculator)
    - [Crazy Buttons](#crazy-buttons)
    - [Stopwatch](#stopwatch)
    - [Accordion](#accordion)
    - [Scrolling Progress](#scrolling-progress)
  - [Reflection](#reflection)
  - [Acknowledgements](#acknowledgements)

## The Projects

### Pricing Calculator

In this project, I made a simple pricing calculator using form inputs for price and quantity.  Once the HTML was ready, I used JavaScript to grab the elements, add event listeners, and write functions that would execute upon interaction with the elements.  As the price and quantity are adjusted, the total cost changes.

![Pricing Calculator Demo](assets/pricing-calculator-demo.gif)

### Crazy Buttons

This was a fun little project that combined simple HTML, CSS, and JavaScript to make buttons that run away from the mouse upon hover.  Once again, after the elements were styled and ready, I grabbed them in the JavaScript and added event listeners and a function to randomize their positions on `mouseenter`.  

The randomized positioning was done with `Math.random()` multiplied by the height or width of this window (minus the button size).  What I liked about this calculation is there are two options to refer to the button size: 

1. Pass in `e` and use `e.target` to refer to the current button
2. Use `this` to refer to the current button

In past projects I've used `e` a lot, so it was neat to apply `this` here.

![Crazy Buttons Demo](assets/crazy-buttons-demo.gif)

### Stopwatch

In this project, I whipped up a simple stopwatch that includes start, stop, and reset buttons that operate a timer.

One concept that I enjoyed about this project was the `pad()` function which makes sure that the seconds and minutes always have two digits each.  So, instead of showing `0:0`, `0:1`, etc., the timer would show `00:00`, `00:01`, etc.

Another concept that was helpful was the use of the `isRunning` boolean to return the start and stop functions so that multiple timers wouldn't be incrementing in the background.

I also appreciated that the `setInterval()` function was separated from `incrementTimer()` in order to keep the code clean and keep track of `interval` when calling `clearInterval(interval)` to stop the timer.  I'm a fan of small, easy-to-read functions.

Finally, I liked seeing an example of using JS `data-` attributes to grab an element.  If I were doing this on my own, I would have add an ID, so it was nice to see this alternative when you want to create custom attributes with JS.

![Stopwatch Demo](assets/stopwatch-demo.gif)

### Accordion

The accordion project was pretty neat because the CSS carried as much weight as the JS to make it work.  In it, there are 3 simple questions that the user can click to make answers appear.  I added the functionality that only one answer can be open at a time, though it's possible to change that so you can have as many open as you'd like at a time.

In the CSS, I liked using `transform` to make the chevron icons rotate when opening and closing.  I also liked getting a little practice with `cubic-bezier` as a `transition` value to customize the timing of a transition.

I used an `open` class to style a list item with the answer showing.  In the JS, instead of adding and removing the `open` class with two separate functions to make the list items open and close, I used `toggle()`.

A neat little trick I used in this project was to `console.log(this)` to see what `this` refers to.  In `toggleAccordion()`, `this` referred to the `question` element, but I needed it to refer to the `li` element.  I used `this.parentNode` to do just that.

![Accordion Demo](assets/accordion-demo.gif)

### Scrolling Progress

This nifty component features an indicator that fills up based on how much you have scrolled through a given article.  While simple, the logic behind it is neat.

3 variables - `windowHeight` (the height of the window), `fullHeight` (the height of the page including the parts hidden before scrolling), and `scrolled` (how many pixels the document is currently scrolled from the top of the viewport) - are used to calculate the `percentScrolled` and update the indicator.

In order to help the program run efficiently when working with larger pages, the `debounce()` function from the Lodash library is used to limit how often the indicator updates.  I used the default wait time of 15 milliseconds.

![Scrolling Progress Demo](assets/scrolling-progress-demo.gif)

## Reflection

Overall, this was a fun collection of projects.  Though they were simple, they each had little helpful tidbits that I can take with me into future projects.

My favorite applications were the use of `this` in place of `e.target`, custom `data-` attributes in JavaScript, the `pad()` function to maintain time format, and the `debounce()` function from the Lodash library.  I also liked learning more about `cubic-bezier()` and working the DOM with `this.parentNode`.  Working with `window` in multiple ways was also helpful.

As a bonus, I learned how to make GIFs to demo all the components.  Not too shabby.

In the future, I'd like to dive into more complex interactions and logic.  The Lodash library sounds like something that would be super helpful for this.  Looking forward to what's next!

## Acknowledgements

Shoutout to [Chris Sev](https://chrissev.gumroad.com/) for his course [Getting Started with JavaScript](https://chrissev.gumroad.com/l/getting-started-with-javascript/).  He does a good job simplifying JavaScript concepts and then applying them to fun mini-projects like these.

Another shoutout to [Codefi CodeLabs](https://www.codelabsdash.com/) for putting together this course and pulling in the best resources for learning software development.  The code coaches and this semester's cohort have been awesome to work with.
