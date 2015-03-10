#CSS TrickShots Part 1

##Introduction
- CSS gives us a ton of tools regarding layout, responsive design, and ui components.
- In addition to this however CSS allow us to do some pretty neat things like animations and transforms.

##Why CSS Animation over JavaScript?
- CSS animations are handled by the native browser code.
- This means that instead of JavaScript dynamically changing `style` attributes over a period of time, the animation is performed graphically via the C++ or Java code that runs the browser.
- This produces an animation that is smoother and more robust than anything we can do with JS.

##The `transition` Property
- CSS animations are handled usually by slowly going from one state to another.
- Think of a div for example that upon hover increases its width. A CSS transition essentially makes the process go in slow motion.
- As a result, we can use transitions to animate between many different states.
- Let's take a look at the syntax:

```
transition: property duration easing;
```

- The property here is the specific CSS property you want to animate. This can be a width, height, color, etc.
- If you want to animate across many properties at the same time you can simply specify `all` instead of an actual property name.
- The duration is the length of the animation. It is specified in seconds.
- The easing is the character of the animation. It allows the animation to look more natural by changing its speed of execution dynamically throughout the duration. Here are the allowed values:
	- ease (default)
	- linear
	- ease-in
	- ease-out
	- ease-in-out
	- cubic-bezier(n,n,n,n)

##Transition Fallbacks
- It is also important to note that transitions are relatively new. As a result, certain older browsers may have limited support.
- To reduce the chance of a transition failure, developers normally add "fallbacks" for older browsers.
- These are usually vendor prefixes:

```
transition: width 1s linear;
-webkit-transition: width 1s linear;
-moz-transition: width 1s linear;
-o-transition: width 1s linear;
```

- It is good practice to always put these in when you use transitions.

##The `transform` Property
- Transforms allow you to temporarily change or warp elements to create neat effects.
- Let's take a look at the syntax:

```
transform: transform-function;
```

- This property makes use of transform "functions" that accomplish the effects.
- Here is a list of commonly-used transform functions:
	- translate
	- rotate
	- scale
- A more exhaustive list can be found [here](https://developer.mozilla.org/en-US/docs/Web/CSS/transform).
- Let's say that we wanted to rotate an element upon hover:

```
#my-div {
	width: 200px;
	height: 200px;
	border:#000 1px solid;
	background-color:#900;
}

#my-div:hover {
	transform: rotate(180deg);
}
```

- As you can see, the div rotates instantly. How do you think we can animate the rotation instead?

##Animate.css
- Animate.css is a library that packages a number of useful animations that can be accessed via classes.
- You can check it out [here](http://daneden.github.io/animate.css/).
- To use this in conjunction with jQuery, there is a great plugin we can use [here](https://github.com/craigmdennis/animateCSS).

##Personal Landing Page Lab
- In this lab we will create a personal landing page.
- Your mission is to use Bootstrap, jQuery, and any CSS animations to create a compelling and interesting personal home page.