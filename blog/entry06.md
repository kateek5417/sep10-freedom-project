# Entry 6
##### 5/1/24

Building my MVP

## My Building Process
The first thing that I did was create the title image and text as well as the navbar. I did this first so that I would have an idea of how the structure of the beginning and the content under it would go. And though I did plan my wireframe out previously, I had trouble envisioning my website until I built the header. After the header I focused on adding the main content and information of my topic  of my pages before I added anything else. I didn't want everything to be on one long page so I divided the different sections into different pages of Home, Present, and Future. As I worked I changed things a bit from the wireframe plans because I had different ideas while typing. When I finished adding the main texts and info for all three pages, I went back to my Present page to put the paragraphs into accordians and the functions of my future technology into bootstrap lists. Then I added the bootstrap cards at the bottom of all three pages as link cards.

## Header
For my header I went with my go to title over a background image style and I found some inspiration for my title's style at [W3schools](https://www.w3schools.com/howto/howto_css_image_transparent.asp). For my titles I used the help of W3school's [image over text](https://www.w3schools.com/howto/howto_css_image_text.asp) to have my text appear on top of the image as well as being centered in the middle. 
``` css
.title-text {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    color: #f1f1f1;
}
```
Then to have a dark background opacity for the title I once again used the help of W3school:
``` css
.text-background {
    background: rgb(0, 0, 0);
    background: rgba(0, 0, 0, 0.5);
    padding: 30px;
}
```

## Main Content
In my Present page I wrote about the different types of veterinary technology that we currently have and them into their separate [bootstrap accordians](https://getbootstrap.com/docs/5.3/components/accordion/) to organize them better without having them taking up too much space. For example:
```html
    <div class="accordion" id="accordionPanelsStayOpenExample">
        <div class="accordion-item">
            <h2 class="accordion-header">
            <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-          target="#panelsStayOpen-collapseOne" aria-expanded="false" aria-controls="panelsStayOpen-collapseOne">
                The Merck veterinary Manual
            </button>
        </div>
    </div>
<!--content-->
    <div class="accordion" id="accordionPanelsStayOpenExample">
            <div class="accordion-item">
                <h2 class="accordion-header">
                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-          target="#panelsStayOpen-collapseTwo" aria-expanded="false" aria-controls="panelsStayOpen-collapseTwo">
                    The Merck veterinary Manual
                </button>
            </div>
    </div>
<!--content-->
```
In my Future page I wrote about the possible future tech for veterinary we could have and I used [bootstrap's list group](https://getbootstrap.com/docs/5.3/components/list-group/) to list the functions of the inventions. For example:
```html
<h4>Functions</h4>
                <ul class="list-group">
                    <li class="list-group-item">The drones would use GPS to navigate between locations more efficiently by selecting the fastest and safest routes while also avoiding any obstacles, this also allows for farther distances.</li>
                    <li class="list-group-item">To avoid the risk of running out of power mid deliver, the drones will be powered by eco-friendly solar panels.</li>
                    <li class="list-group-item">There will an app where users connect with vets to order prescribed drugs from pharmacies to avoid the trouble of pick ups. Refills can also ordered after consulting with the vet.</li>
                    <li class="list-group-item">Users will be able to track their delivery with quick on-the-spot GPS tracking on both the drone and their package.</li>
                </ul>
```
## Navigational Cards
At the bottom of every page I put two of [bootstrap's cards](https://getbootstrap.com/docs/5.3/components/card/) so that the user could use them to navigate to either other two pages of the website. They are also used to add a little bit more style to the pages. 
``` html
<div class="container">
            <div class="row">
                <div class="col col-lg-6 col-sm-12">
                    <div class="card" style="width: 30rem;">
                        <img src="img/card/life-saving-hospital-equipment.jpg" class="card-img-top">
                        <div class="card-body">
                            <h5 class="card-title">The Present</h5>
                            <p class="card-text">Get to know some of the modern technology in medicine.</p>
                            <a href="present.html" class="btn btn-primary">Continue</a>
                        </div>
                    </div>
                </div>
                <div class="col col-lg-6 col-sm-12">
                    <div class="card" style="width: 30rem;">
                        <img src="img/card/future-tech-card.webp" class="card-img-top">
                        <div class="card-body">
                            <h5 class="card-title">The Future</h5>
                            <p class="card-text">Take a peek in to my imagination of the future of veterinary technology.</p>
                            <a href="future.html" class="btn btn-primary">Continue</a>
                        </div>
                    </div>
                </div>

            </div>
        </div>
```

## Challenge
A challenge I had while making my MVP was with the shape of my title background opacity. For my title text I used the background text opacity css from w3schools to make my title pop out from the dark background image and the background stretches from one side of the screen to the other. I didn't like how thin and stretched out the background opactiy was for larger screens but I wanted to keep it as it was for smaller screen sizes. They way I coded the background opacity was with a `background` and `padding` property on a class on parent `<div>` that contained the title texts.
``` css
.text-background {
    background: rgb(0, 0, 0, 0.5);
    padding: 30px;
}
```
So then I tried messing around with the padding, height, and width, but I coldn't figure out how to make it so that the `css` would only be applied to a certain screen size.
That was when I remembered the use of media queries and their function of applying certain `css` for specific sizes. To refresh my knowledge of media queries I looked back at my notes and [RWD Media Queries](https://www.w3schools.com/css/css_rwd_mediaqueries.asp) at w3schools.
It took some trial and error to get the size requirements right and when I did I wrote the `css` I wanted for medium screen sizes and smaller.
```css
@media (max-width: 992px) {
    .text-background {
        padding: 30px;
        width: 100%
    }
}
```





[Previous](entry05.md) | [Next](entry07.md)

[Home](../README.md)
