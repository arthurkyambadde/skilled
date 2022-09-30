# Frontend Mentor - Skilled e-learning landing page solution

This is a solution to the [Skilled e-learning landing page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/skilled-elearning-landing-page-S1ObDrZ8q). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

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
- [Acknowledgments](#acknowledgments)

## Overview

- The Skilled e-learning landing page challenge on Frontend Mentor is a perfect challenge if you now have a solid understanding of HTML & CSS fundamentals. Personally am using (`SASS, SCSS and HTML5`) and all it's mordern modules for the page styles to archieve a design close to the figma design as possible.

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![Skilled e-learning landing page - Desktop version](./src/assets/Screenshot%20Desktop%20Frontend%20Mentor%20Skilled%20e-learning%20landing%20page.png)
![Skilled e-learning landing page - Tablet version](./src/assets/Screenshot%20Tablet%20Frontend%20Mentor%20Skilled%20e-learning%20landing%20page.png)
![Skilled e-learning landing page - Mobile version](./src/assets/Screenshot%20Mobile%20Frontend%20Mentor%20Skilled%20e-learning%20landing%20page.png)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

- Innitially I downloaded starter files from Frontend Mentor and began building the web page by formatting the index file and using semantic tags to handle various components of the page. Am using the **BEM** modal for my HTML.

- Atfer writing some markup, I wrote a (`package.json`) file to assist compile my SCSS to CSS and for SASS am going with the modern SCSS modules of **@forwards & @use** statements.

- For the webpage styling, SCSS file structure am going with a (`7 - 1 file & folder structure)` pattern since it's more handy for the **BEM** modal and allows you to easily refactor, organize and structure your code in a way that is clear easy and simple to navigate.

### Built with

- Semantic HTML5 markup
- CSS Custom Properties
- SCSS variables
- Flexbox
- CSS Grid
- Desktop-first workflow

### What I learned

- I have managed to revive and upgrade on my knowledge of SASS, SCSS in the project by researching about the best way to compile your SCSS into CSS and discovered that using an extension is not so efficient for it makes working on one project for more than one developer difficult for you can't export any JSON file for others to know which dependencies you using on a certain project and you have to explicitily inform the other developers the extensions you using on a certain project which is not practical.

- Inorder to address the mentioned issue I installed a JSON file to assist me set up some dependecies that will always watch my SCSS declaration and compile them to CSS

- I also researched and learnt the mordern current ways of doing stuff in SCSS, where am not to use **@import** but rather use **// @forward and @use instead**

```scss
@forward "./";
@use "./";

@mixin respond($breakpoint) {
  @if $breakpoint == phone {
    @media (max-width: 37.5em) {
      @content;
    } //600px
  }
  @if $breakpoint == tab-port {
    @media (max-width: 56.25em) {
      @content;
    } //900px
  }
  @if $breakpoint == tab-land {
    @media (max-width: 75em) {
      @content;
    } //1200px
  }
  @if $breakpoint == big-desktop {
    @media (min-width: 112.5em) {
      @content;
    } //1800
  }

  // in the file
  @include respond(phone) {
    // padding: 1.6rem;
  }
}
```

### Continued development

This is my first project to deal with responsive images in a way of helping the browser render images dynamically based on the view-port width using the Html `<picture></picture>` tag and this concept is still challenging to me and am planning to keep practising this concept in my future projects till I fully understand the `<source />` tag and all it's attributes such as the `srcset` and many more.

### Useful resources

- [Stop using an extension to compile Sass - Kevin Powel](https://www.youtube.com/watch?v=o4cECvhrBo8) - This wonderful video assisted me so much to know the right way to compile your SCSS code into CSS without running into issues that come along with extensions.

- [Stop using @import with Sass | @use and @forward explained - Kevin Powel](https://www.youtube.com/watch?v=CR-a8upNjJ0&t=51s) - This is an amazing youtube video assited me to know how to write SCSS partials and imports using the current SCSS modules

-[Minimum Static Site Setup with Sass](https://thinkdobecreate.com/articles/minimum-static-site-sass-setup/) - This amazing article helped me to write my **package.json** file and ensure that my SCSS code is being compiled correctly into CSS

## Author

- Website - [Add your name here](https://www.your-site.com)
- Frontend Mentor - [@ssembatya-dennis](https://www.frontendmentor.io/profile/ssembatya-dennis)
- Twitter - [@DennisSsembatya](https://twitter.com/DennisSsembatya)
