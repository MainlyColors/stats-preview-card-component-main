# Frontend Mentor - Stats preview card component solution

This is a solution to the [Stats preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/stats-preview-card-component-8JqbgoU62). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size

### Screenshot

![Desktop Design JPG](/design/final-desktop-design.jpg?raw=true "Desktop Design")
![Mobile Design JPG](/design/final-mobile-design.jpg?raw=true "Mobile Design")

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Stats-Preview-Card-Component](https://ryan2505.github.io/stats-preview-card-component-main/)

## My process

1.  To tackle this challenge I started with looking over the design files to plan out how to structure the HTML. In the beginning I went with a CSS grid solution but later refined it to just use CSS flexbox because it greatly simplified shifting the image from the right side in the desktop design to the top in the mobile design.

2.  After laying out the HTML semantically as I knew how. I wrote the CSS for the desktop design first, I know there is a big emphasis on mobile-first design but I think desktop approach with keeping in mind it will shrink down to mobile is easier think out without the experience.

3.  I really tried to make the design as fluid as possible with CSS clamp(), min(), and max() functions but the biggest problem was sizing the <img> to shrink correctly. I was trying to get the img to zoom in towards the center as the container shrunk so more screen sizes could be supported instead the (2) final designs. After nothing working for many different attempts and trying to research why the img didn't want to behave correctly, I gave up to avoid wasting anymore hours and removed my clamps for the other elements to reinforce the (2) designs only. I'm sure i'll come across the solution later in another project or Javascript/ a service to serve different size images based on viewport size might be the solution.

4.  After writing the desktop design, I used a media query to create the mobile design at (max-width: 1300px) because the design starts breaking at that size. for the most part thanks to CSS flexbox my media query css was relatively minimal with a few weird property's required to overwrite the desktop values.

5.  When I finished both designs, I added some scrollbar styling for when the mobile design view height doesn't fit completely. Similar colors in the design were used for the scrollbar to keep the same style.

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Reponsive design

### What I learned

- ✨ During this project I learned about using the _<picture>_ tag in HTML to dynamically serve the correct size image based on screen size parameters. In the below HTML we use the _<source>_ tag to define options for each parameter defined with the _media_ attribute then use the _scrset_ attribute to give the image location. For browsers that don't support _<picture>_ or when the parameters can't be matched, we include a default _<img>_ tag.

```html
<picture>
  <source media="(max-width: 1300px)" srcset="./images/image-header-mobile.jpg" />
  <source media="(max-width: 1440px)" srcset="./images/image-header-desktop.jpg" />
  <img src="./images/image-header-desktop.jpg" alt=" 3 women working on computers" />
</picture>
```

### Continued development

- ⚠ For the future I want to better understand why I couldn't dynamically control the img to size correctly for a more fluid design. It's probably something simple I'm just missing but I'll look more into the issue in isolation later.

### Useful resources

- [Solutions to common struggles](https://youtube.com/playlist?list=PL4-IK0AVhVjMbyomzxwNOECQwioJLxX6n) - I felt really stuck at the beginning trying to force a fluid grid layout but this playlist by [Kevin Powell](https://www.youtube.com/kepowob) really helped ground some basic concepts so I could move on.

- [Flexible layouts without media queries](https://blog.logrocket.com/flexible-layouts-without-media-queries/) - In the beginning I was trying to avoid media queries which was unavoidable in the end by this article introduced new concepts I was able to incorporate in my design.

## Author

- Frontend Mentor - [@ryan2505](https://www.frontendmentor.io/profile/ryan2505)
