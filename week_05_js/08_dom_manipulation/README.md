#JavaScript Continued

##Array Functions

####.push()

The `.push` method allows you to add new items to the end of an array and returns the new length.

```
var myArray = ["Apple", "Banana", "Orange"];

myArray.push("Grape", "Peach");
```

####.pop()

The `.pop` method removes the last element of an array and returns that element. This will actually change the array.

```
var myArray = ["Apple", "Banana", "Orange", "Grape"];

myArray.pop();

//Array is now ["Apple", "Banana", "Orange"];
```

####.shift()

The `.shift` method removes the first element of an array and returns that element. This will also change the array.

```
var myArray = ["Apple", "Banana", "Orange", "Grape"];

myArray.shift();

//Array is now ["Banana", "Orange", "Grape"];
```

####.unshift()

The `.unshift` method adds one or more elements to the beginning of an array and returns the length of the new array. This will change the array.

```
var myArray = ["Apple", "Banana", "Orange", "Grape"];

myArray.unshift("Peach");

//Array is now ["Peach", "Banana", "Orange", "Grape"];
```

####.forEach()

The `.forEach` method executes a provided function once per array element.

Let's say we want to display the result of adding 2 to each index of the below array:

```
var myArray = [1, 2, 3, 4];

myArray.forEach(function(element, index, array) {
	console.log(element + 2);
});
```

####.map()

Array mapping allows you to create a new array from running some provided function on each index of the given array.

Let's say we want to multiply every number in the below array by 2 to produce a new array:

```
var myArray = [2, 3, 4, 5];

var newArray = myArray.map(function(currentValue, index, array) {
	return currentValue * 2;
});
```

####.reduce()

Array reduce allows you to run a function on all array indexes and return a single value. Let's say we wanted to add together all of the items in this array:

```
var myArray = [2, 3, 4, 5];

var sum = myArray.reduce(function(previousValue, currentValue, index, array) {
	return previousValue + currentValue;
});
```

##Array Exercises

1. Find the last name in the following array:

```
var friends = [
    'Moe', 
    'Larry', 
    'Curly',
    'Jane',
    'Emma',
    'Elizabeth',
    'Elinor',
    'Mary',
    'Darcy',
    'Grey',
    'Lydia',
    'Harriet'
];
```

2. Add your name to the end of the friends and add another name to beginning. Change the Elizabeth to Liz.
3. Sort the list of friends above.
4. There are a list of names in a string, below. How could we sort them? Hint: use string and array methods.

```
var friends = "Moe,Larry,Curly,Jane,Emma,Elizabeth,Elinor,Mary,Darcy,Grey,Lydia,Harriet";
```

5. List all the friends above in reverse alphabetical order.

##Objects

####Object Notation

```
var myObject = {
	firstName: "Arun",
	lastName: "Sood",
	role: "Instructor"
};
```

####Accessing Objects

```
myObject.firstName

myObject.lastName

myObject.role
```

####Objects can have multiple data types

```
var myObject = {
	firstName: "Arun",
	lastName: "Sood",
	sayName: function() {
		alert(this.firstName + " " + this.lastName);
	},
	age: 27
};
```

####`this` keyword
- `this` refers to the current object scope.
- In the case of `myObject` above, the current scope is `myObject`.
- I could have simply referred to it by `myObject`, but `this` is very DRY.
- You will see this syntax very often in "MVC"-type JavaScript frameworks such as Backbone.js.

##Object Exercises

1. How would you represent the following using and object literal. Then update john's address to 1234 Park ln.

```
John, Doe, 36, 1234 Park st.
```

2. Using a combination of Objects and Array, how would you represent the following:

```
Moe, Doe, 31, 1234 Park st.
Larry, Doe, 36, 1234 Spark st.
Curly, Doe, 36, 1239 Park st.
Jane, Doe, 32, 1239 Spark st.
Emma, Doe, 34, 1235 Spark st.
Elizabeth, Doe, 36, 1234 Park st.
Elinor, Doe, 35, 1230 Park st.
Mary, Doe, 31, 1231 Park st.
Darcy, Doe, 32, 1224 Park st.
Grey, Doe, 34, 1214 Park st.
Lydia, Doe, 30, 1294 Park st.
Harriet, Doe, 32, 1324 Park st.
```

##Introduction to DOM Manipulation
- One of the most powerful features of JS is its ability to alter the DOM.
- You can respond to events on elements, set HTML dynamically, and perform animations.

##Selecting Elements
- Like CSS, if you want to perform some action on an element you first have to select it.
- We did this in CSS through selectors such as IDs, classes, and pseudo-selectors.
- JavaScript gives us an easy way to select elements based on the same paradigm.

####getElementById()

```
document.getElementById("my-div");
```

####getElementsByClassName()

```
document.getElementsByClassName("my-div");
```

####getElementsByTagName()

```
document.getElementsByTagName("my-div");
```

####querySelector()

```
document.querySelector("#my-div");
```

####querySelectorAll()

```
document.querySelectorAll("#my-div.my-class");
```

##Handling Events
- There are many events you may want to respond to with JS including clicks, mouseovers, focuses, etc.
- Events can be listened for and responded to using `addEventListener`.

```
document.getElementById("my-div").addEventListener("click", function() {
	alert("Click worked!");
});
```

- If you need to handle an event that occurs on many elements you will need to attach event listeners to each element individually.
- This can be done by binding the event to a class. Let's take this example:

####index.html

```
<div class="my-div"></div>
<div class="my-div"></div>
<div class="my-div"></div>
```

####app.js

```
var myElements = document.getElementsByClassName("my-div");

for (var i = 0; i < myElements.length; i++) {
	myElements[i].addEventListener("click", function() {
		alert("Click worked!");
	});
}
```

##innerHTML
- When you need to replace the HTML inside of an element you can use the `innerHTML` property.

```
document.getElementById("my-div").innerHTML = "<span>New HTML here</span>";
```

##Score Keeper Lab / Homework
- We will be creating a simple score keeper application using JavaScript.
- The HTML and CSS has already been done for you [here](score_keeper_html/).
- Here are the steps you should take:
	- Step 1: Add a link to your own custom JS file before the closing body tag.
	- Step 2: Bind click events to the +5 and -5 point buttons and change the innerHTML of the score display appropriately.
	- Step 3: Bind a click event to the set score button and set the innerHTML of the score display to the score entered in the text box.
	- **Bonus:** Create a check in your code to make sure the score will not go negative.
	- **Super Bonus:** Create a function to make the changes to the score display rather than having to write your logic over and over.