# Frontend Mentor - Profile card component solution

This is a solution to the [Profile card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/profile-card-component-cfArpWshJ). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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

- Build out the project to the designs provided

### Screenshot
![Desktop-view](./Desktop-view.png)
![Mobile-view](./Mobile-view.png)

### Links

- Solution URL: (https://github.com/dev-radex/profile.git)
- Live Site URL: (https://profca.netlify.app/)
## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Desktop-first workflow

### What I learned

I learned how negative values combine with `position: absolute` and `transform: rotate()` to place decorative elements exactly where I want them, even partly off-screen.

By giving `.top` and `.bottom` negative `top`/`bottom`/`right` values, I could push the background SVGs outside the visible card area so only part of the pattern peeks in — instead of being constrained to positive offsets inside the container.

```css
@media (max-width: 600px) {
  .bottom {
    width: 600px;
    height: 600px;
    transform: rotate(13deg);
    bottom: -160px;
    right: -314px;
  }
  .top {
    width: 600px;
    height: 600px;
    transform: rotate(-22deg);
    top: -242px;
  }
}
```

I also used `rotate()` inside a media query to re-angle the patterns for smaller screens, since the rotation that looked right on desktop needed adjusting once the layout and image size changed at 600px.

### Continued development

Going forward, I want to focus more on responsiveness — getting comfortable enough with media queries that I'm not just patching values after the fact, but planning breakpoints and layout changes from the start.

I'd also like to get more comfortable using CSS features like `transform`, `translate`, and `rotate` in general. I used them here, but mostly by trial and error rather than a solid mental model of how they interact with `position: absolute`. I want to reach the point where I can predict the result before tweaking numbers in the browser.

### Useful resources

- [Master CSS Transform Property: Rotate, Scale, Translate & Skew Tutorial](https://www.youtube.com/watch?v=ZSQuEAVEHGs&t=123s) - This helped me understand how `transform` (translate/rotate) works with `position: absolute`, and I'll keep using this pattern for positioning decorative elements going forward.

## Author

- Frontend Mentor - [@dev-radex](https://www.frontendmentor.io/profile/dev-radex)
- Twitter - [@radex_xo](https://www.twitter.com/radex_xo)

