# Tool Learning Log

Tool: **Animate.css**

---

2/29/24:
* I practiced applying animations to my html by using them on one of my old projects, the movie webpage. I create my own copy so I could tinker without worrying about breaking something on the official project. The webpage was for a horror movie so I wanted to add some animations for some spooky ambiance while also drawing the viewer's attention on certain things like the title of the movie.
* I added a pulse animation to the title with `animate__animated animate__pulse`, repeated it twice with `animate__repeat-2`, and slowed it down with `animate__slower` to give it a floating-ghost feel to it.
* I also added a fade in animation with `animate__fadeIn` for a `<span>` to give it a mysterious effect
  

3/1/24:
* Whenever I used the pulse animation it would always create a horizontal scroll bar at the bottom of the screen whenever it ran and I've been trying to find a way to get rid of that. The official Animate Style website says to use the css property `overhidden: hidden` to hide the scroll bar but it didn't work.
* I tried to dive deeper into it by searching "animation.css overflow hidden" but the results I got were irrelevant to my issue or they used what I think was a different coding language all together.
* Then I tried to search more about the `overflow` property itself and found a page dedicated to the property on [W3schools](https://www.w3schools.com/css/css_overflow.asp). It mentions that that `overflow` only works for block elements with a specified height. However, even after adding a `height` property to my animated element, the scroll bar at the bottom of the screen.
* But the `height` property gave me an idea: if the animation is creating a scroll bar because it's overflowing, why don't I just make sure it doesn't overflow in the first place?
* After using the `width` property and adjusting the size, it turned out that the scroll bar was from the animation exceeding the screen's size, so setting a smaller width to the element solved the issuse. Though I mostly just found a cheaty alternative, I at least some sort of solution to my problem.

3/9/24
* This whole time I've been animating text elements but I wondered whether I could also animate images.
* Applied `animate__animated animate__tada` to give it the "tada" animation and it worked
* The animation classes and properties works the same say on images as they do on other elements

3/10/24
* I wondered what else I could and couldn't animate so I apllied animation classes to a bunch of different elements.
* The elements I tested out are: `<p>`, `<span>`, `<div>`, `<body>`
* Of the elements that I tried to animate only `<span>` was not able to be animated

3/18/24
* As we continue to learn more about Bootstrap, I then wondered if I could animate Bootstrap components.
* i added a button component to my file and attached a `backInUp` entrance to it
  ```html
  <div class="dropdown">
    <button class="btn btn-secondary dropdown-toggle animate__animated animate__backInUp" type="button" id="dropdownMenuButton" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
      Dropdown button
    </button>
  ```
* The button animated properly
* I learned that I could animate Bootstrap components

  3/18/24
  * There was this constant little voice in the back of head that kept talking about the `overflow` property and how I didn't figure out how to use it so I tried again.
  * Even though I used my "cheaty" way of preventing scroll bars from appearing during certain animations they still appeared so now I was determined to learn how to properly remove them.
  * Turns out I just didn't read close enough to the directions because the website says to apply the property to the animated element's _parent_ container, this was just a huge face palm moment.
  * So instead of putting the `overflow` property directly into the animated element, I put it into a parent `div` container and it worked
  ```html
  <div>
    <p class="animation"> Lorem Ipsum </p>
  </div>
  ```
  ```css
  div {overflow; hidden;}
  ```
  
3/24/24
* I was scrolling through the different animations and was trying them out when I came across the hinge animation that didn't work quite the same as it did on the official site. In my tinkering the animaion would be too "big" and when I compared it to the website's animation I had a sneaking suspision that the point at which the animation hinged on was the corner of its container. My suspisions were confirmed when I made the border of my elemnet solid, the hinge point was in fact the top left corner of the container.
* To fix this I just made the margin smaller to better fit the text
  ```css
  .animate__animated.animate__hinge {
      width: 10%;
    }
  ```
* However, while I was tinkering around with the hinge animation, I noticed that the text with the animation couldn't be centered even if I used
  ```css
  * {text-align: center;}
  ```

3/24/24
* I can use the "attention seeker" animations to make certain things stand out but I also wonder if it is possible to make it so that an animation starts only when the element is clicked. For example, when a button is clicked the `bouce` animation would play.
* I tried to google "animate.style animation start when clicked" but the results were things I was unfamiliar with or not what I looking.
* Most used `javascript` like [this website](https://stackoverflow.com/questions/4847996/css-animation-onclick), or they created animations from scratch using `html` and `css` like [here](https://amp.dev/documentation/guides-and-tutorials/develop/animations/triggering_css_animations) but none of them use the `Animate.style` tool that I am using

3/29/24
I practiced using Animate.style by applying it on to my SHABR project.
* Following the theme of hot air balloons, I decided to have the title text bounce up to the screen with `animate__bounceInUp`
  ```html
  <div class="title-text animate__animated animate__bounceInUp">
    <h1 class="title-font">Skydance Hot Air Balloon Rides</h1>
    <h2 class="title-font">Ride with the wind Dance with the sky</h2>
  </div>
  ```
    * But applying the animation did something to the position of the text towards the right side of the screen so I used trial and error to adjust the `css` property to return the text back to its location.
    * It turns out that I just to change the `left: 50%;` to `left:10%;`
    * ```css
      .title-text {
        position: absolute;
        top: 50%;
        left: 10%;
      }
      ```
* I thought it would be nice to have the clipart logo in the navbar animated so I applied the `animate__bounce` class
  ```html
  <a class="navbar-brand" href="#">
    <img src="hot-air-balloon-clipart.png" alt="clipart icon" class="navbar-icon animate__animated animate__bounce">
  </a>
  ``` 
* I applied the attention seeker HeartBeat animation on all of the `<h1>` headers to make the beginning of each new section pop out
  ```html
  <h1 class="section-header animate__animated animate__heartBeat">Fun for Everyone!</h1>
  <h1 class="section-header animate__animated animate__heartBeat" id="info">All the information you'll need</h1>
  <h1 class="section-header animate__animated animate__heartBeat" id="gallery">Gallery</h1>
  <h1 class="section-header animate__animated animate__heartBeat" id="testimonials">Just a few of our happy customers</h1>
  <h1 class="section-header animate__animated animate__heartBeat">We'd love to hear from you</h1>
  ```
* While adding animations do add more "life" in to the websites, all of the animations load at the beginning when the website loads in so viewers can't see any of the animations that are lower
  

<!-- 
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
