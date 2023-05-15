# Frontend Mentor - Chat app CSS illustration solution

This is a solution to the [Chat app CSS illustration challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/chat-app-css-illustration-O5auMkFqY). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshots](#screenshots)
  - [Links](#links)
- [My process](#Process-and-workflow)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview - Chat app CSS illustration Master

Here you can find my solution to the Chat app CSS illustration Master coding challenge which is to implement the design in the given images and to illustrate the Chat app page using CSS and to make it fully responsive to all screen sizes, and to animate the chats.
- Given were these two JPEG design images for mobile & desktop layouts:

![Mobile design image preview for the Chat app CSS illustration coding challenge](./design/mobile-design.jpg) ![Desktop design image preview for the Chat app CSS illustration coding challenge](./design/desktop-design.jpg)

### The challenge

Users should be able to:

- View the optimal layout for the component depending on their device's screen size
- See the chat interface animate on the initial load

## The challenge details

Build out this feature illustration using HTML & CSS and get it looking as close to the design as possible.

The only assets provided in this challenge were the image of the person in the app UI and the 3 images of the dog. I needed to create everything else using HTML & CSS!

Users should be able to:

- View the optimal layout for the component depending on their device's screen size
- See the chat interface animate on the initial load

### Screenshots

Screenshots from my solution:

- Desktop screen:

![](<./Snapshots/Desktop/Screenshot%202022-06-17%20at%2016-09-15%20(latest)%20Frontend%20Mentor%20Chat%20app%20CSS%20illustration.png>)

- Mobile screen:

![](./Snapshots/Mobile/Screenshot%202022-06-17%20at%2016-34-10%20Frontend%20Mentor%20Chat%20app%20CSS%20illustration.png)

### Links

- Solution URL: [Solution](https://github.com/Rami24t/Chat-app-CSS-illustration_Frontend-Mentor-Challenge)
- Live Site URL: [Live site](https://rami24t.github.io/Chat-app-CSS-illustration_Frontend-Mentor-Challenge)

## Process and workflow

- Initialized project as a public repository on [GitHub](https://github.com/).
- Configured repository to publish code to a web address.
- Looked through the designs to start planning out how I'll tackle the project and think ahead about CSS classes.
- Before adding styles, I structured my content with HTML first which helped me focus my attention on creating well-structured content. I thought ahead and gave the necessary classes to the HTML tags.
- Wrote out the base styles for the project, including general content styles.
- Started adding styles to the page moving from one section to the next.
- I first styled the mobile version and then did the desktop one.
- I revisited and retouched each section and feature as necessary.

- After finishing the HTML structure and adding all the images and text, I started working on the styling. I first did the paragraph with its title including the fonts and then moved to illustrating the mobile chat app in the mobile screen starting from top to bottom. After that I created the background illustrations using CSS and then worked on retouching and spacing the screen and paragraph and putting it all together on both screens. I also added the bonus 'See the chat interface animate on the initial load' feature by making and adding the necessary animations. I also needed to make custom designed radio buttons. I also crafted the shape used in the buttons and the one used before the avatar image and the three dots and the designs in the background using CSS and HTML.

- After I was finally satisfied with the result which was as close as possible to the two given images on the two different screens. I took some screenshots of the final results and added them to the (./Snapshots) folder.
- I deployed my project using github and github pages.
- I submitted and shared my solution.

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow

### What I learned

- I learned and practiced and gained lot of project-making and especially frontend web-development and CSS/HTML design skills whilst the making of this project.
  It was fun and challenging, especially the parts where I had challenge myself to create everything that was needed by using pure CSS.
- The element creation parts such as illustrating the mobile screen or the elements used inside it and inside the app and illustrating the background shapes on different screen sizes, and the Chat animation were most fun and needed some imagination. Making it look perfect on both screens was also a nice challenge. The custom radio buttons were also interesting to illustrate.
- It was generally a much fun and rich HTML/CSS challenge.

- Code Snippets:

- Here is how I did the background shapes for the mobile screen:

```html
<div class="bg-shapes">
  <div class="bg-shape-violet"></div>
  <div class="bg-shape-grey"></div>
</div>
```

```css
.bg-shape-violet {
  position: absolute;
  background: linear-gradient(to top, var(--violet) 28%, var(--magenta));
  left: -150vw;
  top: -20vh;
  bottom: 31vh;
  right: 50vw;
  border-radius: 0% 0 38% 0%;
}

.bg-shape-grey {
  position: absolute;
  background: var(--app-background);
  left: 50vw;
  top: 60vh;
  bottom: -50vh;
  right: -130vw;
  border-radius: 36% 0 0 0;
}
.bg-shapes {
  position: absolute;
  top: 0%;
  right: 0%;
  left: 0%;
  min-height: 100vh;
  z-index: -8;
  overflow: hidden;
}
```

- Since I am using mobile first approach. I needed to add the necessary changes to the styling of the background and other elements of the desktop and bigger screens by using min-width media queries:

```css
@media only screen and (min-width: 500px) {
  .bg-shape-violet {
    ...;
  }
  .bg-shape-grey {
    ...;
  }
  ...;
}
@media only screen and (min-width: 1340px) {
  .main-container {
    display: flex;
    ...;
  }
  .bg-shape-violet {
    ...;
  }
  .bg-shape-grey {
    ...;
  }
}
```

- Here is how I made the three dots symbol:

```html
<div class="three-dots">
  <div class="circle"></div>
  <div class="circle"></div>
  <div class="circle"></div>
</div>
```

```css
.three-dots {
  margin-left: auto;
  margin-right: 0.1rem;
}
.circle {
  height: 2px;
  width: 2px;
  background-color: white;
  border-radius: 50%;
  margin: 2px;
}
```

- Here is how I coded the bonus feature of animating the chats on the initial load

```css
.received:nth-child(2) {
  animation: receive-anim 0.1s linear 0.2s 1 backwards;
  transition: all 0.4ms;
}
.received:nth-child(4) {
  animation: receive-anim 0.1s linear 0.7s 1 backwards;
  transition: all 0.4ms;
}
.sent:nth-of-type(4):nth-child(6) {
  animation: send-anim 0.1s linear 1.7s 1 backwards;
  transition: all 0.4ms;
}
.sent:nth-of-type(3) {
  animation: send-anim 0.1s linear 2.2s 1 backwards;
  transition: all 0.4ms;
}
.sent:nth-of-type(4) {
  animation: send-anim 0.1s linear 2.7s 1 backwards;
  transition: all 0.4ms;
}
.received:nth-of-type(5) {
  animation: receive-anim 0.1s linear 3.7s 1 backwards;
  transition: all 0.4ms;
}
.received:nth-child(13) {
  animation: receive-anim 0.1s linear 4.2s 1 backwards;
  transition: all 0.4ms;
}
.received:nth-child(14) {
  animation: receive-anim 0.1s linear 4.8s 1 backwards;
  transition: all 0.4ms;
}

@keyframes receive-anim {
  from {
    transform: translateX(-110%) scale(0.1);
    display: none;
  }
}
@keyframes send-anim {
  from {
    transform: translateX(110%) scale(0.1);
    display: none;
  }
}

.grey-chat:nth-of-type(1):nth-child(1) {
  animation: show-typing 0.33s linear 1;
  visibility: hidden;
  position: absolute;
  z-index: -9;
  transform: translateX(-5%);
  width: 4.6rem;
  text-align: center;
}
.grey-chat:nth-of-type(2):nth-child(3) {
  animation: show-typing 0.38s linear 0.45s 1;
  visibility: hidden;
  position: absolute;
  z-index: -9;
  transform: translateX(-7%);
  width: 4.6rem;
  text-align: center;
}
.grey-chat:nth-of-type(7) {
  animation: show-typing 0.39s linear 3.4s 1;
  visibility: hidden;
  position: absolute;
  z-index: -9;
  transform: translateX(-9%);
  text-align: center;
  width: 4.6rem;
}
.white-chat {
  --position-v: 0.3rem;
}
.white-chat:nth-of-type(3):nth-child(5) {
  animation: show-typing 0.4s linear 1.4s 1;
  position: absolute;
  margin-top: 0.6rem;
  right: 0rem;
  text-align: center;
  visibility: hidden;
  opacity: 0.8;
}
.white-chat:nth-of-type(5):nth-child(7) {
  animation: show-typing 0.4s linear 1.9s 1;
  position: absolute;
  right: 0rem;
  text-align: center;
  visibility: hidden;
  opacity: 0.8;
}
.white-chat:nth-of-type(6) {
  animation: show-typing 0.4s linear 2.3s 1;
  position: absolute;
  right: 0rem;
  text-align: center;
  visibility: hidden;
  opacity: 0.8;
}

@keyframes show-typing {
  to {
    visibility: visible;
    transform: translateX(0%);
    right: var(--position-v);
  }
}
/* typing-ani */
.typing-dots {
  margin-left: 0.1rem;
  width: 4.6rem;
}
.typing {
  display: inline-block;
  width: 6.5px;
  height: 6px;
  margin-right: 5%;
  border-radius: 49%;
  opacity: 0;
  transform: translateY(-110%);
}
.grey-chat .typing {
  background: var(--mod-violet);
}
.white-chat .typing {
  background: hsla(271, 15%, 43%, 0.9);
}
.typing.typing-1 {
  animation: typing 1.45s infinite forwards;
}
.typing.typing-2 {
  animation: typing 1.45s 0.2s infinite forwards;
  margin-right: 5.5%;
}
.typing.typing-3 {
  animation: typing 1.45s 0.5s infinite forwards;
}

@keyframes typing {
  to {
    transform: translateY(85%);
    opacity: 0.6;
  }
}
```

- I coded and custom styled the radio button visuals using the label's pseudo class:

```css
.option > label::before {
  border: 2px solid var(--r-btn-outline);
  border-radius: 50%;
  content: "";
  left: -25px;
  bottom: 1px;
  width: 11px;
  height: 11px;
  position: absolute;
  opacity: 0.9;
  box-shadow: 0px 0px 1px #d444f5;
  pointer-events: none;
}
```

- Code snippet of the options and the buttons in the chat app:

```html
          <label for="op30m" class="option received">
            <input type="radio" name="option" id="op30m" />
            <label for="op30m">30 minute walk </label>
            <p>$29</p>
          </label>
          <label class="option received" for="op1h">
            <input type="radio" name="option" id="op1h" />
            <label for="op1h">1 hour walk </label>
            <p>$49</p>
          </label>
          <hr>
          <div class="input">
            <input type="text" name="message" placeholder="Type a message… ">
            <button>
              <div class="greater-symbol">></div>
            </button>
            </input>
          </div>
```

```css
button {
  border-radius: 50%;
  background-color: var(--ddd-violet);
  color: var(--white);
  border: none;
  height: 1.85rem;
  width: 1.85rem;
  overflow: hidden;
  text-align: center;
  padding: 4px 4px 6px 6px;
  position: absolute;
  right: 10.6%;
  top: 55%;
  transform: translateX(50%) translateY(-50%);
}
.greater-symbol {
  font-size: 1rem;
  font-weight: 700;
  transform: scaleY(1.5) scaleX(0.77);
  text-align: center;
  overflow: hidden;
  text-rendering: geometricPrecision;
  opacity: 0.98;
}
button:active .greater-symbol,
button:active .greater-symbol::after {
  opacity: 0.8;
  cursor: pointer;
}
.greater-symbol::after {
  content: ">";
  cursor: pointer;
  position: absolute;
  transform: translateX(-100%) scaleY(1.1) scale(1.1) translateY(-3%);
  opacity: 0.6;
}

.option {
  background-color: var(--magenta);
  background-image: linear-gradient(to right, var(--magenta), var(--violet));
  border-radius: 20px;
  margin: 0.6rem auto 0.6rem 0.6rem;
  width: max-content;
  border-radius: 12px 12px 12px 5px;
  font-size: 0.63rem;
  color: var(--white);
  padding: 10px 21px 9px 6px;
  line-height: 1.4;
  gap: 8px;
  min-width: 10.6rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.option > label {
  margin-right: auto;
  position: relative;
}
.option > input[type="radio"] {
  opacity: 0.01;
  filter: hue-rotate(70deg) contrast(80%) brightness(1.2);
  fill-opacity: var(--magenta);
  position: relative;
  transform: scale(1.5) translateY(-2px);
}
.option > label::before {
  border: 2px solid var(--r-btn-outline);
  border-radius: 50%;
  content: "";
  left: -25px;
  bottom: 1px;
  width: 11px;
  height: 11px;
  position: absolute;
  opacity: 0.9;
  box-shadow: 0px 0px 1px #d444f5;
  pointer-events: none;
}
input[type="radio"]:checked + label::before {
  background: radial-gradient(#fff 58%, var(--r-btn-outline-2));
}
.option > p {
  font-size: 0.886rem;
  font-weight: 700;
  color: var(--white);
}
```

### Continued development

In the projects after this one I am using a broader tech stack and including CSS frameworks such as Tailwind and more Javascript projects.

### Useful resources

- [w3schools](https://www.w3schools.com/Css/) - This is an amazing resource which helped me realize that it is best to make my own custom radio buttons. I'd recommend it to anyone who needs a hint on styling elements.

## Author

- Github - [Rami Al-Saadi](https://github.com/Rami24t)
- Linkedin - [Rami Al-Saadi]https://www.linkedin.com/in/rami-al-saadi-16a14223a/
- Frontend Mentor - [@Rami24t](https://www.frontendmentor.io/profile/Rami24t)

## Acknowledgments

I would like to thank Frontend for offering the exercise and Github for offering the hosting and w3schools for offering their tutorials.

- July 2022 - Rami Al-Saadi
