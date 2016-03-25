**WDI Fundamentals Unit 5**

---

#####By the end of this Unit, you'll be able to:
* Define a function with one or more parameters
* Execute a function within a program or in the console
* Given a function and a set of arguments, predict the output of a function
* Use selectors and methods to access and update the DOM

---

# Functions

You've had an opportunity to see some functions in the homework assignments at the end of units 3 and 4; now it's time to learn about writing them!

But first... a little math.

**Function** is a term that comes out of mathematics - you may remember seeing it in a high school algebra class. The basic idea of a function is simple - it's a relationship between a set of inputs and a set of outputs.

Consider the relationship between a variable `x` and the function `f`. The function `f` takes the input `x` and spits out a single output (`f(x)`).

<br>
<center><img src="../assets/chapter5/function.png"></center>
<br>

If we were shown the output (`f(x)`) for each value of `x`:

| x  | f(x) |
|:-: |:-:   |
| -1 | -2   |
| 0  | 0    |
| 1  | 2    |
| 2  | 4    |
| 3  | 6    |

We could figure out that the relationship between `x` and `f(x)` is that the output is equal to double the input.  In algebra, this relationship is written as `f(x) = 2 * x`. Nothing unfamiliar going on here, right?

Functions play a similar role in programming – JS Functions, like mathematical functions, perform transformations. They take input values and return an output value.



# The Document Object Model

In previous units, we've relied on `console.log` and `alert` to give feedback to users. Later in this unit we'll look at how we can provide more meaningful feedback and make our sites more "user friendly" by allowing users to interact with our site and see its contents updated in real time.

Let's take a look at the following HTML page:

```html
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<title>To Do List</title>
</head>
<body>
	<h1>Things To Do</h1>
	<ul>
		<li>Call Mom</li>
		<li>Take out the trash</li>
		<li>Return library books</li>
	</ul>
</body>
</html>
```

This HTML page is simply a text document written in a language the browser understands. It uses opening and closing tags to provide structure and give meaning to the content of the page.

The browser pulls in this HTML document, parses it, and creates an object model of the page in memory. This model is called the **Document Object Model (DOM)**. 

The DOM specifies that the browser should use a **DOM Tree** to structure this model:

<br>
<center><img src="../assets/chapter5/dom.png"></center>
<br>

Each element in the HTML document is represented by a **DOM node**. You can think of a node as a live **object** that you can access and change using JavaScript. When the model is updated, the changes are reflected on screen.

We can get and set attributes for these nodes – perhaps we want to add a class or update styling to make an item fade in or out. We can access and change the content – maybe we want to change the text in the third `li` to read "Return library books - DONE!" Or we can even add new nodes or remove nodes from the page.

Once we get some functions under our belt we'll take a look at how we can use some of JavaScript's "built-in" functions to interact with the DOM and add some more complex interactions to our sites.

Ready to dig in? [Let's take a look at functions.](02_lesson.md)
