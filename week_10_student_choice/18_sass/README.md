#Introduction to SASS / SCSS

##What is SASS?
- SASS or otherwise known as SCSS stands for Syntactically Awesome Stylesheets.
- It is an alternate way of writing CSS code that makes it cleaner and more efficient especially while working on large applications.
- This alternate syntax is then "compiled" or re-formatted into standard CSS code before you show it in the browser.
- Let's also check out the [SASS website](http://sass-lang.com/).

##Why SASS?
- SASS keeps your code cleaner. For example, let's say that you want to create a uniform look and feel throughout your site with a set of colors. Instead of having to repeat the colors over and over throughout your styles, you can set them up once, which will affect the whole stylesheet.
- Bootstrap, Foundation, and a bunch of other front end frameworks were created with SASS. This allows you to customize them heavily.
- Many backend languages integrate well with the language. Rails for example has built-in support.

##The SASS Command Line
- SASS is a Ruby gem. Let's install it together:

```
sudo gem install sass
```

- To make sure it's installed:

```
sass -v
```

- When you write in the SASS syntax, you need to compile it to standard CSS before running it. There are two ways this can be done:

####Manually

```
sass input.scss output.css
```

####Set up a watch

```
sass --watch input.scss:output.css
```

- SASS watch is a great tool that monitors for changes in the source files and automatically compiles to CSS when a change is detected. This is useful for development.

##Variables
- Variables in SASS allow us to set up certain property values that can be used throughout the stylesheet.
- A good example would be if you wanted to set up a font color that you want to use in a few different classes.

####base.scss

```
$my-fonts: Arial, Helvetica;
$my-size: 20px;
$cool-color: #06C;

.class1 {
	font-family: $my-fonts;
	font-size: $my-size;
	color: $cool-color;
}

.class2 {
	font-family: "Times New Roman", Arial;
	font-size: $my-size;
	color: $cool-color;
}
```

##Nesting
- Another useful tool of SASS is nesting. Nesting allows you to write CSS in a way that makes sense visually.
- Let's say that you wanted to write style properties for any divs inside of the class `my-class`. We could do this:

```
.my-class {
	div {
		background-color: red;
		padding: 20px;
	}
}
```

##Partials
- Partials let you take code from a separate SCSS file and include it in your base file.
- This allows you to be able to write code pertaining to certain sections of your site, which is then wrapped into the main code when it is run.
- This is heavily used in Bootstrap's source files, where each piece of the framework is broken out into its own separate file.
- Let's take a look at an example:

####_header.scss

```
nav {
	background-color:#000;
	padding:20px;
}
```

####_footer.scss

```
footer {
	padding:20px;
	background-color:#CCC;
	font-size:2em;
}
```

####main.scss

```
@import "partials/header";

@import "partials/footer";
```

##Mixins
- Mixins allow you to write code once and repeat it throughout your CSS.
- A good example of using this would be for the border-radius property:

```
@mixin border-radius($radius) {
	-webkit-border-radius: $radius;
	-moz-border-radius: $radius;
	-ms-border-radius: $radius;
	border-radius: $radius;
}

.box {
	@include border-radius(10px);
}
```

##Blog Template Exercise
- For this exercise we will be using the starter code located [here](blog_template/).
- Take a look at the way the page looks now. We are going to try our best to emulate the look and feel with SASS.
- Copy the files to another directory and create at least one SCSS file to work from.
- Try to use the existing HTML coupled with your own SCSS to create the same effect.
- Use at least:
	- Nesting
	- 1 Mixin
	- 1 Partial