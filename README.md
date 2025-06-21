# Frontend Mentor - Product preview card component solution

This is a solution to the [Product preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover and focus states for interactive elements

### Links

- Live Site URL: (https://cool-mochi-8b2214.netlify.app/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

```html
<figure class="mobile-img">
  <img src="./images/image-product-mobile.jpg" alt="Mobile Perfume">
</figure>
<figure class="desktop-img">
  <img src="./images/image-product-desktop.jpg" alt="Desktop Perfume">
</figure>

Quick way to switch between photos using two classes and hiding one when the media query is activated.
```

```css
html, body {
    height: 100%;
    margin: 0;
}

-Defaulted height to 100% to ensure website contents take up full height of the viewport.

body {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    background-color: var(--cream);
}

-Flex display to align contents.

.card {
    background-color: var(--white);
    display: grid;
    max-width: 22rem;
    border-radius: 10px;
    margin: auto 0.75rem;
}

-Applied grid with no defined cells (places all content in one cell).
-Applied max-width to .card to prevent image from oversizing past the width.
-Applied minor margin auto to width to centralize it, and 0.75rem to height to give it its own 'padding' (instead of body {padding: ...}).


figure {
    padding: 0;
    margin: 0;
    height: auto;  
}

figure img {
    border-radius: 10px 10px 0 0;
    max-inline-size: 100%;
    display: block;
    max-height: 250px;
}

-Styled figure (image container) with no padding/margin for image to take up whole space
-Height auto so height responds to contents
-Max-inline-size 100% so image takes up 100% of the width of figure.
-Max-height 250px to constrain image.

@media (min-width: 548px) {
    .card {
        display: grid;
        grid-template-columns: 1fr 1fr;
        min-width: 37rem;
    }

    figure img {
        border-radius: 10px 0 0 10px;
        aspect-ratio: 1 / 1;
        min-height: 100%;
    }
}

-Gives card two columns - 1 for image, 1 for content (row form)
-Min-width 37rem to ensure image is always appropriate size.
-Figure img given aspect ratio of 1 / 1 to ensure a good image resolution
-Min-height: 100% so it takes up all of figure constantly.

```

Improving at Responsive Design now.

### Continued development

Still need to improve at Responsive Design, and maybe typography and use of responsive units, breakpoint setting.

### Useful resources

- (https://webgrowth.co.uk/technical-seo-tip-use-css-swap-images-mobile-desktop-users/#:~:text=You%20can%20use%20CSS%20to,size%20of%20the%20user's%20device.&text=Have%20unique%20classes%20for%20the%20mobile%20and%20desktop%20div.&text=The%20%40media%20is%20a%20rule,it%20is%20called%20media%20queries.) - Used this website for swapping device images using CSS and Media Queries.

## Author

- Frontend Mentor - [@lemz100](https://www.frontendmentor.io/profile/lemz100)
