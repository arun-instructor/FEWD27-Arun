#Introduction to SASS / SCSS

##What is SASS?
- SASS or otherwise known as SCSS stands for Syntactically Awesome Stylesheets.
- It is an alternate way of writing CSS code that makes it cleaner and more efficient especially while working on large applications.
- This alternate syntax is then "compiled" or re-formatted into standard CSS code before you show it in the browser.

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