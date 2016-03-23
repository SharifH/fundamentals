# Navigation & Page Layout Homework

Having learned about layout, we are even better equipped to structure the HTML of our game.

## Exercise

#### Requirements

Currently, the cards in your game are all awkwardly formatted vertically and styling is seriously lacking. Start by changing the orientation of the cards so that they are structured into a conventional two by two grid layout. Next, create a navbar for the game that would serve to link to the `Instructions` and `Game` sections as if they were on two separate pages. Further, your navbar should be styled in a way that lets users know when they are hovering over a clickable item. It's always great to keep the User Experience (UX) in mind! Finally, be sure to add some color to your footer.

**bonus:**

- Use the navbar items to [scroll down](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a) to their respected positions on the page.

##### Below are the steps to complete the assignment.

1)

```css
.board {
  height: 50%;
  width: 50%;
  display: inline-block;
}

.card {
  height: 200px;
  width: 150px;
  border-radius: 10px;
  border: 1px solid black;
  background-size: cover;
  float: left;
  margin: 8%;
}
```

2) Add your nav and anchor elements.

```html
...
  <body>

    <nav>
      <a href="#">Instructions</a>
      <a href="#">Game</a>
    </nav>

    <header>
...
```

3) Style your navbar by removing default stylings, adding colors (including a hover state) and positioning your navbar items.

```css
...
      nav {
        background-color: #808080;
      }

      a {
        background-color: #ffbf00;
        color: white;
        text-decoration: none;
        display: block;
        float: left;
        padding: 35px;
      }

      a:hover {
        background-color: #ee5f3c;
      }
...
```

4) After you floated your nav items you should have noticed how your header became wrapped around the side of it. Can you remember the CSS solution to this problem? The infamous `clearfix` class.

```html
...
  <body>

    <nav class="clearfix">
      <a href="#">Instructions</a>
...
```

```css
...
      .clearfix:after {
        visibility: hidden;
        display: block;
        content: " ";
        clear: both;
        height: 0;
        font-size: 0;
      }
...
```

5) All that's left to do is to finish off your footer with some background-color.

```css
...
footer {
  background-color: #808080;
}
```


#### Deliverable

Congratulations! Your board game is now structured and styled utilizing all your new knowledge of HTML and CSS!

![](https://s3.amazonaws.com/f.cl.ly/items/0g1W0p28360L253L1X0v/Image%202016-03-23%20at%207.20.53%20AM.png?v=c0763f91)