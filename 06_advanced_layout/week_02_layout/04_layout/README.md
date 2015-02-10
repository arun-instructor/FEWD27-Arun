#Layout With HTML and CSS

##Quick Warmup
- Let's use Codepen.io to practice CSS selectors.
- Create at least one div with an id, and four divs with a class.
- Use CSS to apply styling to the divs based on the id and class selectors.
- Bonus: Try implementing one or more styles using a CSS3 selector (first-child, nth-child, first-of-type, etc).

##Floats
- Floating elements allows us to create a nearly unlimited number of layouts using all types of block elements.
- Floating an element essentially removes it from the standard "flow" and places it to the left or right side of its container.
- Elements can have fixed width, which will wrap underneath each other if the container is smaller than the combined widths.
- You can also used percentage width, which will have the columns respond to the screen size.
- You can tell already that the calculations can get out of hand really fast...

##Element Alignment
- To determine how we can align an element we have to first know what kind of element it is.
- Inline elements can be aligned as text, so with the `text-align` CSS property.
- Block elements can be aligned using the space around them - margin. A margin set to auto for both left and right will center the element in a container.

##The Grid Layout
- Most modern layouts operate on a standard 12-column grid system.
- If you break down any of the websites you know and love you will notice many variations on the 12 column grid.
- Each column in the grid can contain nested grids itself.
- If you want a larger box, you need to have a greater column offset.
- Here is a good pictorial to help you break it down:

![Grid Pictorial](img/grid.jpg)

##Group Exercise
- In groups of two, look up one website of your choice.
- Think about the layout they chose in terms of the grid system.
- Write down which column "offsets" were likely used, and where nested grids may be present.
- Review the mockup of the fashion blog part 2 located [here](img/fashion_blog_2.png) and do the same thing.

##Code-Along: Let's Create Our Own Grid
- We will create a 2, 4, and 6 column grid.
- We will try nesting a grid inside another grid.

##CSS Positioning
- There are four main types of positioning that you will see most often - static, relative, absolute, and fixed.
- Static positioning is what all elements have by default. Yay!
- Relative and absolute work together - elements can be positioned absolutely relative to their container.
- Fixed position elements are essentially absolute relative to the window no matter where they are in the DOM. A.K.A. the window is always the relative parent.

##Positioning Exercise
- Try to replicate the following mockups using what we've talked about in this class so far.
- Utilize margins, padding, floats, positioning, etc.

1. Stackers!

![Stackers!](img/stackers.png)

2. The Mirror

![The Mirror](img/the_mirror.png)

3. The Skinny

![The Skinny](img/the_skinny.png)

4. The Absolute

![The Absolute](img/the_absolute.png)

##Homework
- For homework you will be creating the fashion blog part 2 using your knowledge of layouts.
- The mockup of what you will be creating can be found [here](img/fashion_blog_2.png).
- Bonus: Implement your own grid system to use in layout.
- Extra Reading: Have a look through the documentation for popular frontend frameworks such as Twitter Bootstrap or Zurb Foundation. Pay attention to how they implement the grid system.
	- [Twitter Bootstrap](http://getbootstrap.com/)
	- [Zurb Foundation](http://foundation.zurb.com/)