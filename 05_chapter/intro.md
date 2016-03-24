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

In previous units, we've relied on `console.log` and `alert` to give feedback to users. In a real-life application, however, we'll want to provide more meaningful feedback and make our pages more "user friendly" by allowing users to interact with our site and see the contents of a web page updated in real time.

When a browser loads a web page, it grabs the page's HTML and creates a model of the page in memory. We can then use JavaScript to access and update the content of this model. When the model is updated, the changes are reflected on screen.

```html
<!DOCTYPE html>
<html>
<head>
	<title>To Do List</title>
</head>
<body>
	<h1>Things To Do</h1>
	<p></p>
	<ul>
		<li>Call Mom</li>
		<li>Take out the trash</li>
		<li>Return library books</li>
	</ul>
	
</body>
</html>
```



html page - nesting and relationships






The Document Object Model (DOM) specifies how browsers should create a model of an HTML page and how we can use a scripting language, such as JavaScript, to access and update the contents of a page.


[Let's take a look.](02_lesson.md)
