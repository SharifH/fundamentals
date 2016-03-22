# Webpage Layout Homework

Having learned about layout, we are even better equipped to format our HTML and uniquely style our game.

## Exercise

#### Requirements

The current state of your game could use some formatting and personalization. Utilize the `header` tag to organize your content by moving the instructions of the game into its own section. It'll be nice to semantically break up your HTML. While you're at it, throw in a horizontal row to help with the cause! Then, to give your webpage a nice personal touch, add a footer which includes some personalized text, something like: `Created with love by <your name>`. Figure out a way to throw in an icon as well and color your name a different color than the rest of the text to give it some oomph. Last but surely not least, give your site a nice touch by centering all if its text.

##### Below are the steps to complete the assignment.

1) Move your heading tags and game instructions into `<header>`.

```html
...
    <header>
      <h1>Memory Game</h1>

      <h2>Instructions</h2>

      <p>
        Concentration, also known as Match Match, Memory, Pelmanism, Shinkei-suijaku, Pexeso or simply Pairs, is a card game in which all of the cards are laid face down on a surface and two cards are flipped face up over each turn. The object of the game is to turn over pairs of matching cards.
      </p>
    </header>
...
```

2) Add a horizontal row underneath your paragraph tag.

```html
...
all of the cards are laid face down on a surface and two cards are flipped face up over each turn. The object of the game is to turn over pairs of matching cards.
      </p>

      <hr>
    </header>
...
```

3) Create your footer with the given text and a heart icon.

```html
...
      <div class="card" id="card4"></div>
    </div>

    <footer>
      Created with &hearts; by <span class="name">GA</span>
    </footer>
  </body>
...
```

4) Wrap your name with `<span>` and give it a class so you can style it.

```html
...
    <footer>
      Created with &hearts; by <span class="name">GA</span>
    </footer>
...
```

5) Go into `style.css` and color your name.

```css
.name {
  color: #ff0000;
}
```

#### Deliverable

Ah! Things are looking better already!

![](https://s3.amazonaws.com/f.cl.ly/items/3k3B3F0W2g2w2m3E2i1q/Image%202016-03-17%20at%209.53.27%20PM.png?v=99531718)