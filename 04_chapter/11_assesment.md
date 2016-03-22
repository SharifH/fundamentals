# Principles of HTML & CSS Homework

From this unit, we have seen how CSS plays a crucial role in the creative aspect of web devlopment. In this homework assignment, you will use your freshly acquired skills to not only create the cards of your memory game, but define a theme to the game.

## Exercise

#### Requirements

Create your cards using images of your choice. Your memory game could consist of a deck of cards, different animals, whatever you like! This is the time you create your theme. Just remember, there are only four cards to the game. Next, start to clean up your code base by moving all your styling into its own separate files. Lastly, change your current named color values to RGB and a Hex values.

**hint:** Your cards should be laid upon a board.

##### Below are the steps to complete the assignment.

1) Create four `div`s each with a class of `card` that are child elements to a `div` that has a class of `board`.

```html
...
    </p>

    <div class="board">
      <div class="card"></div>
      <div class="card"></div>
      <div class="card"></div>
      <div class="card"></div>
    </div>
  </body>
...
```

2) Add unique ids to each card.

```html
...
    </p>

    <div class="board">
      <div class="card card1"></div>
      <div class="card card2"></div>
      <div class="card card3"></div>
      <div class="card card4"></div>
    </div>
  </body>
...

2) Use your id selector to add specific styles to certain elements, in this case card images.

```css
      .card1 {
        background-image: url("https://52cards.files.wordpress.com/2009/05/428px-poker-sm-212-ks.png?w=455");
      }

      .card2 {
        background-image: url("https://upload.wikimedia.org/wikipedia/commons/thumb/d/d3/King_of_clubs2.svg/2000px-King_of_clubs2.svg.png");
      }

      .card3 {
        background-image: url("http://cliparts.co/cliparts/kc8/nxa/kc8nxaMcr.png");
      }

      .card4 {
        background-image: url("https://s-media-cache-ak0.pinimg.com/236x/15/e4/3a/15e43a712ac44407d23c437b0a5b43bc.jpg");
      }

```

3) For styles that are shared across multiple elements you'll want to utilize the the more general selector, class. Since we know all card elements will share certain characteristics such as: width, border-radius, etc., we can go ahead and define these CSS properties to the class, `card`.

```css
.card {
  height: 200px;
  width: 150px;
  border-radius: 10px; /* give the divs card-like rounded corners */
  border: 1px solid black;
}
```

4) Move your CSS from `<style>` to its own file, `style.css`. To connect these styles with your HTMl, use `<link>` to reference it.

```html
<link rel="stylesheet" href="style.css">
```

5) Switch up the named color values to RGB and Hex values. If you can't figure out the exact RGB or Hex value to match the color, don't sweat it, just use something close. The key is just to practice implementing a more technical value.

**tip:** A good way to find your color value would be with a google search, `<color name> hex code` or `<color name> rgb color`.

```css
h1 {
  color: rgb(2, 132, 130);
}

h2 {
  color: #ffd700;
}
```

#### Deliverable

Great! Your website is starting to look more and more like an actual memory game!

![](https://s3.amazonaws.com/f.cl.ly/items/0n1W1M2d0y3f1Q2V1T16/Image%202016-03-17%20at%208.44.47%20AM.png?v=cc378882)