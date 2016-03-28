**WDI Fundamentals Unit 5**

---
#Manipulating the DOM

Now that you've gotten some practice accessing and updating the DOM, let's take a look at some more advanced methods that will allow us to update content and styles.

### Adding Content
####**`createElement()` and `appendChild()`**

To add new elements to the page, we'll need to use a three step process:

1. We will use the `createElement()` method to create a new element, which can then be added to the page. When this node is created, it will be *empty*. This element will be stored in a variable.
2. We will then add content to the element using the `innerHTML` or `textContent` properties we looked at in the last lesson.
3. Now that our element has been created we can add it as a child of an element using the `appendChild()` method. This will add an element as the last child of the parent element.

To add a fourth item to our list we can execute the following code:

```js
// First up, let's create a new list item and store it in a variable.
var newListItem = document.createElement('li');

// Alright! Now let's update the text content of that list item.
newListItem.textContent = 'Feed the cat';

// And Finally...let's add that list item as a child of the ul.
document.getElementsByTagName('ul')[0].appendChild(newListItem);


```
<br>
<center><img src="../assets/chapter5/append_child.png"></center>
<br>

It takes a few steps but you'll get the hang of it in no time.

### Getting and Setting Attributes

We might also want to update styles and attributes for elements on the page. We can do so using the following properties and methods:

####`className`
We can change the value of a class attribute for an element using the `className` property. This will apply any styles in our CSS that are associated with that particular class.

For example, maybe we want to highlight an important task in our list. We can add a class and styles in our CSS like so:

```css
.highlight {
	background-color: yellow;
}
```

And then we can use JavaScript to add this class:

```js
document.getElementById('important').className = 'highlight';

```

The `.highlight` class will then be added to the element with the id `important` and the background-color associated with this class will be applied:

<br>
<center><img src="../assets/chapter5/class_name.png"></center>
<br>

####`setAttribute()`, `removeAttribute()`

We can set and remove attributes from elements using the `setAttribute()` and `removeAttribute()` methods.

For example, if we want to update the `href` attribute on an anchor, we could do the following: 

```js
document.getElementsByTagName('a')[0].setAttribute('href', 'http://newurl.com');

```

Or if we wanted to remove the id from an element we could execute the following:

```js
document.getElementsByTagName('a')[0].removeAttribute('id');

```


#Events

In order to create interactive and responsive sites, we'll often want to update the DOM based on the user's actions. For example, when the user clicks on the menu icon, a sidebar menu should slide out from the side of the page. Or if the user has typed an incorrect format into a form field, the field should be outlined in red as the user tabs out of the field. These actions are called **events**.

We can set up **event handlers** in our scripts that will listen, or wait, for an event to occur and then trigger a function.

The syntax for setting up an event handler looks like this:

```js
  element.addEventListener('nameOfEvent', functionToRun);
```
* `element` - This refers to the DOM node we want to tie the event to. For example, if we want to trigger an event when the user clicks on a button, the element would be that button element.

* `` - The dot ties the method on the right hand side (`addEventListener`) with the element on the left hand side.

* `addEventListener()` - This is the method we will use to tie an event listener to an element.

* `'nameOfEvent'` - The name of the event we want to listen for. For example, maybe we want to wait until the user triggers a 'click' event on an element.

* `'functionToRun'` - The name of the function that we want to run when the event occurs.

Let's take a look at an example:

```js
// Here let's set up a function that will be triggered when the event occurs.
var alertUser = function () {
	alert('Button has been clicked!');
}

// Next let's find the element we want to tie the event to and save it to a variable.
var button = document.querySelector('button');

// Finally let's set up an event handler. When the user clicks on the button, the alertUser function will run.
button.addEventListener('click', alertUser);

```

##Types of Events

There are many events that can be used to trigger a function. Let's take a look at a few:

|  Event      |  Description  |
|:-------:    |:-------:|
| 'click'      | When the button (usually a mouse button) is pressed and released on a single element  |
| 'keydown'     | When the user first presses a key on the keyboard  |
| 'keyup'   | When the user releases a key on the keyboard    |
| 'focus'     | When an element has received focus   |
| 'blur'     | When an element loses focus   |
| 'submit'   | When the user submits a form  |
| 'load'   | When the page has finished loading  |
| 'resize'      | When the browser window has been resized  |
| 'scroll'      | When the user scrolls up or down on the page |


Let's take a look at a practical example. We've created a simple form for users to subscribe to our email newsletter. When the user tabs or clicks away from the email input field, we want to check to make sure that the user has entered a value in the field.

The HTML:

```html
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<title>To Do List</title>
	<link rel="stylesheet" href="style.css">
</head>
<body>

	<form>
		<h1>Email Form</h1>
		<input type="email" placeholder="Email Address">
		<button type="submit">Subscribe</button>
		<p id="message"></p>
	</form>


</body>
</html>

```

Our CSS:

```css
.error {
	border: 1px solid #fa4542;
}
```

And now for our JavaScript:

```js  
// First, let's find the email input field.
var emailInputField = document.getElementById('email');

// Next up, let's set up a function to run when the even occurs.
var checkEmailInput = function () {
	
	// Check to see whether the user has entered a value to the email field.
	if (emailInputField.value.length === 0) {
		// If the email field is blank, display a message to the user.
		document.getElementById('message').innerText = 'Please enter an email address.'

		// Add an error class to the input field that will give it a red border.
		emailInputField.className = 'error';
	} else {
		//Otherwise, clear out the error message.
		document.getElementById('message').innerText = '';

		// Remove the error class from the input field
		emailInputField.className = '';
	}

}

// Finally, let's add our event handler that will trigger the function when the user
// hits tab or clicks out of the email field (the 'blur' event).

emailInputField.addEventListener('blur', checkEmailInput);
```


Let's take a look at what the page now looks like when the focus was on the email field and then the user hit tab or clicked away from the field:
<br>
<center><img src="../assets/chapter5/event_example.png"></center>
<br>

##Conclusion
This is just the tip of the iceberg when it comes to DOM manipulation and event handling. But hopefully it's gotten you excited about making your sites interactive and responsive. There are so many methods and functions to keep track of in the beginning that it can be a little overwhelming. Don't feel like you have to sit down and memorize everything. Instead focus on understanding the big picture and memorization will come with practice.


---

Think you've got it? [Get some practice in the next exercise.](11_exercise.md)