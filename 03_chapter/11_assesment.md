# Introduction to HTML & CSS Homework

In this unit we introduced some of the core fundamentals of web deveplopment including how the internet works as well as how a website is structured and styled. With this newfound knowledge we can go ahead and architect the foundation of our memory card game app, leaving us with something to grow upon in future lessons.

## Exercise

#### Requirements

Firstly, go ahead and set up your game's boiler plate code. Beyond this, make sure to personalize your website by displaying the name of the game in its corresponding browser tab. Further, the name should be displayed as a big header in the content of your site. Also, what good is a game if you don't know how to play? Under your header, include a subheader, "Instructions," and a section explaining how a memory card game is played. Last, but not least, add some flare to the site by adding at least two colors.

**hint:** To add styling within your HTML file add your CSS between `<style></style>` tags.

**bonus:**

- add a subheading describing the game
- add some personal social media links so users can learn about the developer behind the game

##### Below are the steps to complete the assignment.

1) Set up the boiler plate code.

```html
<!DOCTYPE html>
<html>
  <head>

  </head>
  <body>

  </body>
</html>
```

2) Add a `title` element so the name of the game shows in the browser tab.

```html
...
  <head>
    <title>Memory Game</title>
  </head>
...
```

3) The name of your game should be placed within a header tag.

```html
...
  <body>
    <h1>Memory Game</h1>
  </body>
...
```

4) You can use an `<h2>` for your subheader and a `<p>` for your section on the instructions of the game.

```html
...
    <h2>Instructions</h2>

    <p>
      Concentration, also known as Match Match, Memory, Pelmanism, Shinkei-suijaku, Pexeso or simply Pairs, is a card game in which all of the cards are laid face down on a surface and two cards are flipped face up over each turn. The object of the game is to turn over pairs of matching cards.
    </p>
  </body>
...
```

5) Add some paint to the canvas! For now, we'll use the CSS property `color` to give some spice to the headers.

```html
...
  <head>
    <title>Memory Game</title>
    <style>
      h1 {
        color: teal;
      }

      h2 {
        color: gold;
      }
    </style>
  </head>
...
```


#### Deliverable

![](https://s3.amazonaws.com/f.cl.ly/items/2J000u3x2I3S2Z1c0y0M/Image%202016-03-16%20at%201.27.18%20PM.png?v=991ea9bd)