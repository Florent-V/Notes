# Notes CSS

## Tables of contents

1. [Partie 1](#)
2. [Partie 2](#)
3. [Partie 3](#)


##### [Return to Top](#notes-css)
# **A Few layout**

* ## Super centered

``` html
<div class="parent blue" >
<div class="box coral" contenteditable>
:)
</div>
```

``` css
.parent {
display: grid;
place-items: center;
}
```

* ## The Deconstructed Pancake 

``` html
<div class="parent white">
    <div class="box green">1</div>
    <div class="box green">2</div>
    <div class="box green">3</div>
</div>
```

``` css
.parent {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}

.box {
    flex: 1 1 150px; /*  Stretching: */
    flex: 0 1 150px; /*  No stretching: */
    margin: 5px;
}
```
* ## Sidebar Says

``` html
<div class="parent">
    <div class="section yellow" contenteditable>
    Min: 150px / Max: 25%
    </div>
    <div class="section purple" contenteditable>
      This element takes the second grid position (1fr), meaning
      it takes up the rest of the remaining space.
    </div>
</div>
```

``` css
.parent {
    display: grid;
    grid-template-columns: minmax(150px, 25%) 1fr;
}
```
* ## Pancake Stack

``` html
<div class="parent">
    <header class="blue section" contenteditable>Header</header>
    <main class="coral section" contenteditable>Main</main>
    <footer class="purple section" contenteditable>Footer Content</footer>
</div>
```

``` css
.parent {
    display: grid;
    grid-template-rows: auto 1fr auto;
}
```
* ## Classic Holy Grail Layout


``` html
<div class="parent">
    <header class="pink section">Header</header>
    <div class="left-side blue section" contenteditable>Left Sidebar</div>
    <main class="section coral" contenteditable> Main Content</main>
    <div class="right-side yellow section" contenteditable>Right Sidebar</div>
    <footer class="green section">Footer</footer>
</div>
```

``` css
.parent {
    display: grid;
    grid-template: auto 1fr auto / auto 1fr auto;
}
header {
    padding: 2rem;
    grid-column: 1 / 4;
}
.left-side {
    grid-column: 1 / 2;
}
main {
    grid-column: 2 / 3;
}
.right-side {
    grid-column: 3 / 4;
}
footer {
    grid-column: 1 / 4;
}
```
* ## 12-Span Grid

``` html
<div class="parent white">
    <div class="span-12 green section">Span 12</div>
    <div class="span-6 coral section">Span 6</div>
    <div class="span-4 blue section">Span 4</div>
    <div class="span-2 yellow section">Span 2</div>
</div>
```

``` css
.parent {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
}  
.span-12 {
    grid-column: 1 / span 12;
}
.span-6 {
    grid-column: 1 / span 6;
}
.span-4 {
    grid-column: 4 / span 4;
}
.span-2 {
    grid-column: 3 / span 2;
}
/* centering text */
.section {
    display: grid;
    place-items: center;
    text-align: center
}
```
* ## RAM (Repeat, Auto, Minmax)

``` html
<div class="parent white">
    <div class="box pink">1</div>
    <div class="box purple">2</div>
    <div class="box blue">3</div>
    <div class="box green">4</div>
</div>
```

``` css
.parent {
    display: grid;
    grid-gap: 1rem;
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
}
```
* ## Super centered

``` html
<div class="parent white">
    <div class="card yellow">
      <h3>Title - Card 1</h3>
      <p contenteditable>Medium length description with a few more words here.</p>
      <div class="visual pink"></div>
    </div>
    <div class="card yellow">
      <h3>Title - Card 2</h3>
      <p contenteditable>Long Description. Lorem ipsum dolor sit, amet consectetur adipisicing elit.</p>
      <div class="visual blue"></div>
    </div>
    <div class="card yellow">
      <h3>Title - Card 3</h3>
      <p contenteditable>Short Description.</p>
      <div class="visual green"></div>
    </div>
</div>

```

``` css
.parent {
    height: auto;
    display: grid;
    grid-gap: 1rem;
    grid-template-columns: repeat(3, 1fr);
}
.visual {
    height: 100px;
    width: 100%;
}
.card {
    display: flex;
    flex-direction: column;
    padding: 1rem;
    justify-content: space-between;
}
h3 {
    margin: 0
}
```
* ## Clamping My Style

``` html
<div class="parent white">
    <div class="card purple">
      <h1>Title Here</h1>
      <div class="visual yellow"></div>
      <p>Descriptive Text. Lorem ipsum dolor sit, amet consectetur adipisicing elit. Sed est error repellat veritatis.</p>
    </div>
</div>
```

``` css
.parent {
    display: grid;
    place-items: center;
}
.card {
    width: clamp(23ch, 50%, 46ch);
    display: flex;
    flex-direction: column;
    padding: 1rem;
}
.visual {
      height: 125px;
      width: 100%;
}
```
* ## Respect for Aspect

``` html
<div class="parent white">
    <div class="card blue">
      <h1>Video Title</h1>
      <div class="visual green"></div>
      <p>Descriptive text for aspect ratio card demo.</p>
    </div>
</div>
```

``` css
.parent {
    display: grid;
    place-items: center;
}
.visual {
    aspect-ratio: 16 / 9;
}
.card {
    width: 50%;
    display: flex;
    flex-direction: column;
    padding: 1rem;
}
```

##### [Return to Top](#notes-css)
# **Main Title**
* ## Subtitle

``` php
<?php

```