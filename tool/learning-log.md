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
* Then I tried to search more about the `overflow` property itself and found a page dedicated to the property on W3schools. It mentions that that `overflow` only works for block elements with a specified height. However, even after adding a `height` property to my animated element, the scroll bar at the bottom of the screen.
* But the `height` property gave me an idea: if the animation is creating a scroll bar because it's overflowing, why don't I just make sure it doesn't overflow in the first place?
* After using the `width` property and adjusting the size, it turned out that the scroll bar was from the animation exceeding the screen's size, so setting a smaller width to the element solved the issuse. Though I mostly just found a cheaty alternative, I at least some sort of solution to my problem.

* 

<!-- 
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
