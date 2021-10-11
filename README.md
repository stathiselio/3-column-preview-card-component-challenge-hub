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
  - [Continued development](#continued-development)
- [Author](#author)

## Overview

I decided to approach with basic CSS/HTML not to use any bootstrap or Sass. I'm not familiar yet with those and want to build stronger foundations.

There where some differences and some mistakes between free and figma designs so I used my judgement there.

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![](./screenshot.jpg)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

I decided to wrap everything in a section element with class .flex-page in order to center everything on Desktop view using flexbox. It seemed like the best option since I wanted to keep everything inside my main element closer to a real world situation.

I used custom properties for all colors and typography.

```css
:root{
    --clr-primary-300:hsl(31, 77%, 52%);
    --clr-primary-400:hsl(184, 100%, 22%);
    --clr-primary-500:hsl(179, 100%, 13%);

    --clr-neutral-300:hsla(0, 0%, 100%, 0.75);
    --clr-neutral-400:hsl(0, 0%, 95%);

    --ff-accent: 'Big Shoulders Display', cursive;
    --ff-base: 'Lexend Deca', sans-serif;

    --fs-400: 0.9375rem;
    --fs-500: 2.5rem;

    --border-radious: 0.5em;
}
```

Also I made a global button that could be used and would be visible elsewhere in a hypothetical website. The I used custom properties to change the colors for the project.

```css
.btn {
    display: inline-block;
    text-decoration: none;
    color: var(--fg, #333);
    background: var(--bg, #fff);
    border: 2px solid var(--bc, #333);
    padding: 0.8em 2.1em;
    border-radius: 100vw;
    transition: 0.1s ease;
}

.car-type .btn {
    --bg: var(--clr-neutral-400);
    --bc: var(--clr-neutral-400);
}

.car-type .btn:hover,
.car-type .btn:focus {
    color:var(--clr-neutral-400);
    background: transparent;
    border-color: var(--clr-neutral-400);
}

.btn-300 {
    --fg: var(--clr-primary-300);
}
.btn-400 {
    --fg: var(--clr-primary-400);
}
.btn-500 {
    --fg: var(--clr-primary-500);
}
```

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow


### What I learned

I had an issue where text depending on the screen size sometimes would push down a button in one of the car-type elements and the button wouldn't be aligned. I used flexbox on the .car-type and I used flex-grow on the text so that it always uses the available space. This way the buttons are always aligned.

```css
.car-type {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    flex-basis: 100%;
    color: var(--clr-neutral-300);
    padding: 3rem;
}

.car-type p {
    flex-grow: 1;
    padding-bottom: 0.8em;
}
```

Use this section to recap over some of your major learnings while working through this project. Writing these out and providing code samples of areas you want to highlight is a great way to reinforce your own knowledge.

To see how you can add code snippets, see below:

```html
<h1>Some HTML code I'm proud of</h1>
```

```js
const proudOfThisFunc = () => {
  console.log('🎉')
}
```

### Continued development

- CSS custom propetries
- CSS modifiers
- Aligningment children of neighbouring elements


## Author

- Frontend Mentor - [@stathiselio](https://www.frontendmentor.io/profile/stathiselio)

