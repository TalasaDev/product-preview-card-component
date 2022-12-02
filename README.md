# product-preview-card-component
Frontend Mentor NEWBIE FREE Challenge 

# Frontend Mentor - Product preview card component solution

This is a solution to the [Product preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover and focus states for interactive elements

### Screenshot

![](./screenshot.jpg)

![image](https://user-images.githubusercontent.com/119393713/205224508-371537e7-6a10-45f1-b510-b08054f08ebb.png)

![image](https://user-images.githubusercontent.com/119393713/205224634-840905a7-ece3-4955-b66f-ba151c729cb8.png)


### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow


### What I learned

In this challenge I learned how to use use different background images depending on the size of the screen to ensure the responsiveness of the website. This was the biggest issue I experienced to obtain a satisfactory result. There are different ways to do it. The one that worked for this project was: place two containers inside .card-image container, one with the mobile image, and the other with desktop image and set in the main.css "mobile-design first" the display of the desktop img and its container  to "none". In the media query for desktop screen size, reverse it and set the display of the mobile img to none. See the code below for more details:


```` HTML

<div class="card-image">

    <div class="desktop">
      <img src="./images/image-product-desktop.jpg" alt="Gabrielle 
      eau de parfum">
    </div>

    <div class="mobile">
      <img src="./images/image-product-mobile.jpg" alt="Gabrielle Eau de parfum">
    </div>

</div>


``` CSS

/*  MOBILE - FIRST DESIGN  */ 

.desktop,
.desktop img {
  display: none;
}

.mobile {
  display: flex;
  margin: 0;
  padding: 0;
  width: 100%;
  height: 39vh;  
  object-fit: cover;
}


/*  DESKTOP DESIGN  */

@media only screen and (min-width: 600px) {

  .mobile,
  .mobile img {
    display: none;    
  }

  .desktop,
  .desktop img {
    display: flex;
    margin: 0;
    padding: 0;
    width: 100%;
    height: 100vh;  
    object-fit: cover;
  }
}

### Continued development

I need to keep working on how to use images in CSS to gain knowledge to apply more advanced design.

### Useful resources

- [100 Days CSS](https://https://100dayscss.com/) - This helped me to understand how to position a container centered within another container. Very useful to design card components.
- [w3schools](https://www.w3schools.com) - Very good resource to gain better understanding of how to manage to use two differents background images depending of the size of the screen. The one I prefered for its simplicity was:

  <picture class="card-image">
        <source media="(min-width: 250px)" srcset="../images/image-product-mobile">
        <source media="(min-width: 600px)" srcset="../images/image-product-desktop">
        <img src="./images/image-product-mobile.jpg" alt="a bottle of Gabrielle parfum">
  </picture> 


## Author

- Website - [coming soon!!!](https://www.your-site.com)
- Frontend Mentor - [@talasa-dev](https://www.frontendmentor.io/profile/talasa-dev)
- Twitter - [@really coming soon](https://www.twitter.com/yourusername)


## Acknowledgments

This is where you can give a hat tip to anyone who helped you out on this project. Perhaps you worked in a team or got some inspiration from someone else's solution. This is the perfect place to give them some credit.
