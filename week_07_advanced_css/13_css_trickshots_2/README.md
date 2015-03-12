#CSS Trickshots Part 2

##Homework Review
- Last class we built a personal portfolio page.
- Turn to a partner and share your work:
	- What worked well?
	- What was challenging?
	- What technologies did you use?

##Recap from Last Class
- How are transitions used? What is the syntax and how does it work?
- How can we couple transitions with transforms?
- Which transform functions do you remember?
- Spend 10 minutes on CodePen and try a few examples.

##CSS Animations Continued: Keyframes
- Keyframes allow you to perform complex animations using CSS alone.
- The idea is that instead of transitioning an element from one state to another slowly, you are specifying style attributes that must be accomplished during stops along the animation.
- Here is the syntax:

```
div {
	width:100px;
	height:200px;
	background-color:red;
	-webkit-animation:identifier 5s ease-in-out infinite;
	animation:identifier 5s ease-in-out infinite;
}

@-webkit-keyframes identifier {
	0% {
		top:200px;
	}

	25% {
		top:50px;
	}

	75% {
		left:100px;
	}

	100% {
		top:0;
	}
}

@keyframes identifier {
	0% {
		top:200px;
	}

	25% {
		top:50px;
	}

	75% {
		left:100px;
	}

	100% {
		top:0;
	}
}
```

##Keyframes Exercise
- Try out some of the keyframes along with a transform function.
- One idea may be to rotate a div during a keyframe animation.
- Observe what happens as the div is transformed. Is this what you expected? Why or why not?
- **Bonus:** Now take things a step further and integrate keyframes with JavaScript.
	- Bind a click event to a button that adds a class to the div.
	- Your class should play a keyframe animation of its own.
	- Use at least one transform function in your keyframe.

##Media Query Refresher
- Let's review what a media query is and how we use it.
- Work with your partner to create a single div on CodePen that is shown only when the screen is between 700 and 900 pixels wide.

##Media Queries with Bootstrap
- Media queries are a core concept in Bootstrap, and are used extensively throughout the framework.
- If you are comfortable using the Bootstrap pre-defined media query breakpoints then you're in luck. Bootstrap gives us a [few helper classes](http://getbootstrap.com/css/#responsive-utilities-classes) to toggle visibility.
- Let's set up a new Bootstrap project to test out these visibility classes with a single div.

##In-Class Lab / Homework: Redesign the Header
- Media queries play a huge part in making websites ready for mobile.
- As a front end developer you will likely run into many situations where you have to take existing content and transform it into a mobile-ready layout.
- In this exercise we will take a navigation menu already created for you [here](header_redesign/) and redesign it for mobile devices.
- Start by adding your own CSS file so that you can clearly see what code you wrote.
- For this exercise you will want to use either custom media queries or Bootstrap's visibility classes.
- Use your creativity to come up with something enticing.
- **Bonus:** Use jQuery to create the sliding functionality of the standard Bootstrap navbar for your redesigned version.
- **Super Bonus:** If you're really pushing ahead, try implementing Animate.css for some cool effects.

##Further Reading / Next Time:
- We will be going over building forms in next class.
- Have a look over the weekend at these tags specifically:
	- `<input>`
	- `<select>`
	- `<textarea>`
- Have a look at [jQuery AJAX](http://api.jquery.com/jquery.ajax/) since we will be using it to submit the form contents.
- Check out the `.val()` jQuery function to grab form data.