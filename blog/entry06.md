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
In my Present page I put all of the different technologies into their own separate [bootstrap accordians](https://getbootstrap.com/docs/5.3/components/accordion/) to organize them better. For example:
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
In my Future page, I used [bootstrap's list group](https://getbootstrap.com/docs/5.3/components/list-group/) to organize the functions of the inventions. For example:
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
At the bottom of every page I put two of [bootstrap's cards](https://getbootstrap.com/docs/5.3/components/card/) so that the user could use them to navigate to either other two pages of the website.

[Previous](entry05.md) | [Next](entry07.md)

[Home](../README.md)
