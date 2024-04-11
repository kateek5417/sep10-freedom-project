# Entry 5
Learning Animate.styke 4/8/24

## What is Animate.style?
They way that the tool [Animate.style](https://animate.style/) works is through a variety of element classes that determines the animation as well as classes and properties that alter how the animation is displayed. For example, if I were to make it so the header were to slide in from the left, I would apply the `animate__slideInLeft` class to the header. It is crucial to make sure that the class `animate__animated` is also in the class in order for the animation to function.
```html
<hi class="animate__animated animate__slideInLeft"> Hello World </h1>
```
Then if I were delay the animation for 2 seconds and loop it infintely, I would add the `animate__delay-2s` and `animate__infinite` classes.
```html
<hi class="animate__animated animate__slideInLeft animate__delay-2s animate__infinite"> Hello World </h1>
```
However, different animations animate differently so adjustments can be made for corrections.

## How did I learn my tool?
To learn my tool I first read through the [Animate.style](https://animate.style/) website to gain a basic understanding of how the tool works. I then moved onto tinkering with the tool in my IDE workspace where I then messed around with the different classes and properties in Animate.style. I went through the animations that interested me and applied them onto basic elements.
```html
<h1 class="animate__animated animate__heartBeat"
<p class="animate__animated animate__flash"> Flash </p>
```

I continued to do this until I became comfortable with the animations and when I did, I moved onto the different customization classes and properties. I tried nearly all of the classes and properties that Animate.style offered and came across some issues I would then learn to overcome.

After animating simple elements such as paragraphs, `<p>`, and headers, `<h1>`, I decided to move onto something bigger and more complex so I practiced on past projects I did as well as [Bootstrap templates](https://startbootstrap.com/themes). 
For my tinkering on my SHABR project I created a copy of my original file into my sandbox folder where I could break any code I wanted to. There I applied a variety of animations where I thought would bring the website to life as well as to bring attention to certain aspects.
Here are some examples:
```html
 <!-- Features section-->
        <section class="py-5 border-bottom" id="features ">
            <div class="container px-5 my-5">
                <div class="row gx-5  animate__animated animate__fadeInLeft">
```
* This clip of `animate__fadeInLeft` makes it so the entire Feature section fades into the page from the left.

```html
 <!-- Header-->
        <header class="bg-dark py-5">
            <div class="container px-5">
                <div class="row gx-5 justify-content-center">
                    <div class="col-lg-6">
                        <div class="text-center my-5">
                            <h1 class="display-5 fw-bolder text-white mb-2 animate__animated animate__fadeInDown">Present your business in a whole new way</h1>
                            <p class="lead text-white-50 mb-4 animate__animated animate__fadeInDown">Quickly design and customize responsive mobile-first sites with Bootstrap, the world’s most popular front-end open source toolkit!</p>
```
- Here the two `animate__fadeInDown` on both `<h1>` and `<p>` in the header makes it so that the text in the header section fades into the screen from the top, bringing a sense of transition into the website's visuals.

## What did I learn about my tool?
Here are some of the things I kearned throughout nearly six weeks of learning on my own:
- Images and Bootstrap components can be animated the same way as regular `html` code
- Certain animations exceed their element's container so they make horizontal scroll bars at the bottom of the screen when running. The solution to this is to aplly the `css` property `overflow:hidden` onto the parent element of the animated element.
  ```html
  <div>
    <p class="animate__animated animate__pulse">
  <div>
  ```
  ```css
  div {overflow: hidden}
  ```
  This makes it so that the part of the element that overflows from the container is hidden instead of making scroll bars
- Emphasize certain elements I can apply one of the website's attention seeking animations like bouncing a certain header: `<h1 class="animate__animated animate__bounce"> Information </h1>`. Or even a smaller phrase within a text element by animating a `<span>`: `<p>There will be a test on <span class= "animate__animated animate__flash">Tuesday the 2nd</span>.</p>`. This makes the content inside of `<span>` flash.
- Which animations to apply on which part of the website: "Attention seekers" like flash, bounce, and pulse can be applied onto smaller elements like `<h>` and `<p>` to make certain information stand out to the viewer. On the otherhand, "Transistions" can be used on larger elements like `<div>` and `<section>` to animate an entire section for smoother transitions and to bring life into the website.

## EDP
Currently in the Egineering Design Process I am beginning the step of planning out my website's layout on a wireframe. After writing my content, learning my tool, and with all of the knowledge I've built up throughout the school year, I am now ready to start actually creating my project website. Once I finish the wireframes I will then move onto creating the website.

## Skills
While learning how to use Animate.style on my own I used my debugging skill to tinker with different codes and animations to break and learn how to use them. I wasn't afraid of trying and testing out ideas I had whether I knew would work or not. If something didn't work the way I wanted to I would analyze the code I see if I had written something wrong or I would trial and error properties in `css` to correct something. This way I was able to freely tinker and explore my tool however I wanted to.

Another skill I used while learning Animate.style was embracing failure. I wasn't worried about my tinkers not working because the whole point of tinkering is to learn while coding and breaking codes. Even when certain codes wouldn't work the way I wanted to I kept trying to fix it. For example, I struggled with the `overflow` property for a while before I learned it. At some point I had nearly given up and settled for a cheaty solution of a problem I had, but I persevered and eventually taught myself how to use `overflow`. By embracing failures and challenges I push myself to learn new things I didn't before.

## Next step
As we are nearing the end of the school year, it is time that we started building our final project website by starting with a wireframe to plan out our layouts. This will help us gain an idea of how we want our website to look like as well as where our tools will be applied.


[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
