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

In previous units, we've relied on `console.log` and `alert` to give feedback to users. In this unit we'll look at how we can provide more meaningful feedback and make our sites more "user friendly" by allowing users to interact with our site and see its contents updated in real time.

When a browser loads a web page, it grabs the HTML for the page and creates a model of the page in memory. This model is called the **Document Object Model (DOM)**. We can use JavaScript to access and change the content of this model. When the model is updated, the changes are reflected on screen.

In an HTML document, elements can be nested inside of other elements. In the example below, we have three `<li>` elements that are enclosed within an opening `<ul>` tag and closing `</ul>` tag.


```html
<!DOCTYPE html>
<html>
<head>
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

In programming, relationships between the document and elements are often described in similar terms as one would use to describe a family tree.

In the above example we could describe the relationship between the `<ul>` element and the three `<li>` elements as that of parent and children since the `<li>` elements are wrapped by the `<ul>` element.

The relationships between the document and elements in the can be represented using a tree structure:

<br>
<center><img src="../assets/chapter5/dom.png"></center>
<br>


This representation is referred to as the **DOM Tree**. Each element in the HTML is represented by a **DOM node**.

Each of these nodes is an **object** that can be interacted with using JavaScript. We can get and set attributes for these nodes (perhaps we want to add a class or update styling). We can access and change the content (maybe we want to change the text in the third `li` to read "Return library books - DONE!"). Or we can even add or remove nodes from the page.




[Let's take a look.](02_lesson.md)
