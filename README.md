# Frontend Mentor - 3-column preview card component solution

This is a solution to the [3-column preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/3column-preview-card-component-pH92eAR2-). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![](./screenshot.png)

### Links

- [Live site URL](https://keen-ritchie-e4d1ce.netlify.app/)

## My process

### Built with:

- Semantic HTML5 markup
- SCSS
- Flexbox
- Mobile-first workflow

### What I learned

#### Images: mix-blend-mode and picture element quirks

- You can use `mix-blend-mode` and `opacity` along with a `background-color` on the wrapper to colorize an image.
- When an image is inside a picture element, you have to give it a defined `width` to use `object-fit`.

```css
.picture-wrapper {
  background-color: $accent-violet;

  picture {
    width: 100%;
    height: 100%;
    display: flex;
  }

  img {
    mix-blend-mode: multiply;
    opacity: 75%;
    object-fit: cover;
    width: 100%;
    height: 100%;
  }
}
```

#### Conflicts between SCSS functions and CSS functions

- Functions like `min` and `max` are currently duplicated between SCSS and CSS. To ensure the CSS one is used, you can capitalize the function. This is needed because SCSS can't handle functions with certain sets of different units.

```css
.wrapper {
  width: Min(1110px, 90vw); /* capitalized so scss ignores it */
}
```

## Author

- Website - [Travis Ricks](http://travisricks.com/)
