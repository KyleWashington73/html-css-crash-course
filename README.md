# html-css-crash-course
#Notes:
----------------------------------------------------------------------------------
                   THE BUILDING BLOCKS OF THE WEB
HTML= (HyperText Markup Language) *The content of websites.
CSS= (Cascading Stylesheets) *How our websites look.
JavaScript= (Programming language) *Can manipulate HTML and CSS.
----------------------------------------------------------------------------------
                   HTML TERMINOLOGY AND SYNTAX
- BASIC SYNTAX:
Tags= We wrap everything in "tags" to tell the browser what is what(ie. <tag>).
<cover> + </cover>= element. (This is my cover element.)
Other elements used to make a webpage:
<page></page>; <heading></heading>; <subheading></subheading>; <p></p>(paragraph).
*Tags are inside of <>. Closing tags include a forward slash </>. Everything from the opening to the closing tag is an element.
----------------------------------------------------------------------------------                    (basic layout of a webpage)
<!DOCTYPE HTML>= The very first thing at the top of document. Tells the browser that this is an HTML5 document.
<html>= Tells the browser that we are about to start writing HTML. We can actually write HTML, CSS, and JavaScript inside an HTML document. HTML acts as the "root" of our document.
<head>= It contains essential info. More like a brain than a head.
<title>= In the head of the document. Not visible on the page. Shows up in browser tab and search results.
----------------------------------------------------------------------------------

*Headings denote hierarchy and page structure. 
*Six Levels of headings=<h1>,<h2>,<h3>,<h4>,<h5>,<h6> (ends at <h6>).
----------------------------------------------------------------------------------
                     HTML - strong and emphasis   
*Used for creating bold and italic text.
<strong>=Text inside <strong> indicates that it is of strong importance. Browsers make thiis text BOLD.
<em>= The text inside of <em>italics</em> has stress emphasis. Browsers make this italic.
*They are inline elements= Use <strong> and <em> within a paragraph. 
*You must close a <strong> or <em> before the end of your paragraph= <p><strong>Warning:<strong> it's very cold outside.</p>
----------------------------------------------------------------------------------
                     **File Naming and Organization**
                        #1 BE ORGANIZED!!!!!
                  #2 File Names are VERY Important!!!
*File Naming= Keep file name short. * They should be descriptive(i.e. about-us.html).
*No spaces, use underscores or hyphens instead. 
*Use lower case ("About-Us.html" vs. "about-us.html")
*The main folder is the "root" folder.
*The homepage must be index.html.
*index.html must be in the root folder, and not a sub-folder!
----------------------------------------------------------------------------------
                        **Anchors and Attributes**
*Elements can have attributes.
-Attributes are always within the opening tag
*Attributes give extra information to the browser about that element, such as where a link goes, or the location of an image file. Normally followed by an =.
*Some elements require an attribute (ie: href).
*If the page you are linking to is NOT part of your website, it MUST start with http:// or https:// to let the browser know it is an external site that you are linking to.
Visit our <a href="about-us.html">about us</a> page!
Visit our <a href="team/john.html">about us</a> page! 
*Relative Paths= You can link to other pages by simply putting their file name.
----------------------------------------------------------------------------------
                          **Intro to CSS**
*Properties= What we want to change (i.e. color,font-size,font weight).
*Values= What we want to set that property to: font size: 21px; 
----------------------------------------------------------------------------------
                           **CSS Basics**
*font-size- Sets the font size. For now let's stick to px(pixels)
*color- Changes the color of the text.
*background-color- Sets the background color. 
*text-align-Align the text to the left, center, or right.
-Colors can be set with keywords, hex codes, rgb and hsl values.
-Keywords: red, steelblue, hotpink, etc.
*Color Codes are called hexadecimal values #7ab0fb
rgb= Red, Green, Blue  rgb(0,255,0) 
hsl= Hue,Saturatuon, Lightness hsl(240,100%,75%)
----------------------------------------------------------------------------------
                              **Lists**
Lists are used for all sorts of things:
*  Regular bullet and numbered lists.
* Navigations.
* Organizing other content.                        
* Two types of lists: - Ordered lists <ol>.
                      - Unordered lists <ul>.
Each bullet or numbered item is a list item <li>.
                       **Example of an Ordered list**
<ol>
  <li>list item</li>         1.  list item    
  <li>list item</li>         2.  list item  
  <li>list item</li>         3.  list item
</ol>
----------------------------------------------------------------------------------
                              **IMAGES**
- Images are like links, in that they require an attribute to work.
- A link uses the href attribute to link to another file.
- Images use the src attribute, which is short for source.
* The syntax= <img src="image.jpg">
* Images are different from other elements, in that they are self closing:
<img src="image.jpg"> or <img src="image.jpg"/>
*Images not valid without an alt attribute.
*The alt attribute is used to describe the image("a very cute cat").
<img src="image.jpg" alt="a very cute cat">
*If it is a decorative element or logo, it doesn't need alt text (but it dies still require the alt attribute.)= <img src="logo.jpg" alt="">
                                   <img src="decorative-red-ball.jpg" alt="">
---------------------------------------------------------------
    **Practice time instructions**(Come back to later!!!!)
Your job is to create a 3 page website about Earth and Mars.

Use the corresponding .md files for the text of your pages.

- Hashtags indicate headings
    - # title  = h1
    - ### title = h3
- Any text with stars around it *like this* must be italic
- Any text with underscores on both sides of it _like this_ must be bold
- Links are shown like this:  [this text is a link](this-is-where-it-links-to.html)
- The images are are in a folder called 'images' already. Don't forget the `alt` text!
- Lines starting with a hyphen (like this one), are an unordered list

- CSS:
  - Change the font-size of the h1 on all pages to: 60px
  - Change the color of the h1 and all h2 on the mars page to: #d33d1f
  - Change the colors of the h1 and all h2 on the earth page to: #2a8442

* All text has been taken from Wikipedia
* Images:
  - Earth: Photo by NASA on Unsplash
  - Mars: Photo by mohammad alizade on Unsplash
---------------------------------------------------------------
                    **Internal CSS**
-Internal CSS is annoying when you want to reapeat the same change in multiple places.
-We can use a stylesheet, rather than inline styles, to make more global changes.
-We can use an internal stylesheet that is place in the head of our pages.
<head> 
  <style>
    CSS goes here.
  </style>

</head>
---------------------------------------------------------------                    **selectors**  
Selectors=What we are seeking.
Property= The property of the element(s) that we wish to change.
*Declaration= Property value pair.
*Rule= Made up of a selector and property-value declarations.
*Selecting elements= It's very easy.
-Write the element, but without the <>.  a { ... }
 -Do not include the attributes.         p { ... }
 -That's it!                             h2 { ... }   
---------------------------------------------------------------
                   **External CSS**
External CSS= *One file is controlling all of the styles, not the page you are on. If you delete something from the stylesheet, or change something, it is changing for all the pages.*
**
**(HTML PAGE in <head> setion)= <link href="" rel="stylesheet">
Instead of a style element, where we can write the CSS,we can use a link, which links to our CSS file. In the head of our document,we add: 
<!DOCTYPE html>
<html>
    <head>
        <title>All about Mars!</title>
                    *(folder/file)*
       *<link href="css/style.css" rel="stylesheet">
    </head>
    <body>
        <h1>Mars</h1>
</body>        
</html>
---------------------------------------------------------------
          **The Relationship Between HTML and CSS**
*Three primary ways to select something:* (we've seen this one before[external css]). 
-Element selector= 
body {
    background-color: aqua;
    color: rgb(68, 3, 248);
}

a {
    color: rgb(241, 9, 9);
}

h1 {
    color: chartreuse;
}
-Class Selector=
*In CSS, the class attribute is referenced by using a full stop(The . means "intro")
.intro {
  font-size: 18px;
  color: #2b5dad;
}
-ID Selector=
*IDs are a type of attribute we can add to an HTML element.
<p id="intro">...</p>
*An ID is represented by a hashtag:  #intro {
                                     font-size: 18px;
                                     color: #2b5dad;
                                 }
*ID is an individual. Class is a group.
-An ID can only be used one time per page.
-A class can be used over and over again.
(An ID will override a class if they are both selecting the same thing.)
***Classes can be used only once of you want***
*(Be encouraged not to use IDs in CSS.)*
---------------------------------------------------------------
                  **Naming classes and IDs**
-Spaces cause problems!!!
*Like this: ( <div class="a box"> ) = ( .a-box { ... } ).
*Can include numbers in names and class IDs. *Can't be the first character.
---------------------------------------------------------------
                        **Comments**
-Useful way to leave notes to yourself, or others if you're working on a large project.
-Two different ways to write them:( , but they use the same shortcut: D.
*In HTML <!- comment here ->
*In CSS /* comment here */
***Comment shortcuts= cmd + /
                         or
                     ctrl + /
---------------------------------------------------------------
                           **Tags**
- Tags so far: h1 --> h6.
- p
- strong and em 
- a
- ul, ol, and li
- img
* These tags are different because they denote different parts of the website.
- header
- main
- section
- footer
- nav
- div  (generic)
---------------------------------------------------------------
           ** Margins **
 margin: 10px  20px     30px   40px
         top   right   bottom  left
margin: 10px
      all sides
margin:  10px      20px
        top and  left and
        bottom    right
margin: 25px   10px    15px
        top    left   bottom
               and 
               right
*Padding is used to control the posithining of content inside our element.
*It works just like margin in terms of the ling form and shorthand properties.
*Margin= empty space
*Padding= more background




---------------------------------------------------------------
                 **The Box Model-borders**
                        **HTML**
<html>
    <head>
        <title>The box model</title>
        <link href="css/style.css" rel="stylesheet">
    </head> 
    <body>
        <header>
            <h1>Intro to the box model</h1>
        </header>
        
        <main>
            <h2>Width and height</h2>
            <p>All elements have a width and a height.</p>
            <p>We can control the width and the height very easily, but be careful when setting heights on elements, it can get you in trouble!</p>
        </main>
        
        <footer>
            <p>the box model</p>
        </footer>
    </body>
</html>
- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -
                            **CSS**
body {
    background: #333;
    color: white;
}

header {
    width: 100px;
    padding: 20px;
    margin: 20px;
    border: 10px solid yellow;
}
*The total width and height of an element is caculated by adding all the different parts of the element together. The four parts of an element:
* The content itself (what you set the width and the height on)
* The padding
* The border
* The margin
- - - - - - - - - - - 
-Don't forget that margin, padding, and borders add width to the left and the right!
*You can also control the border of the different sides independently:
                .example  {
                  border-left: 2px solid pink;
                  border-right: 5px dotted red;
                  border-bottom: 10px double green;
                  border-top: 1px dashed purple;
                  }
---------------------------------------------------------------
-------------------------------------------------------------
....or create a new repository on the command line.
echo "# wfb" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/KyleWashington73/wfb.git
git push -u origin main
- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - 
...or push and existing repository from the command line.
git remote add origin https://github.com/KyleWashington73/wfb.git
git branch -M main
git push -u origin main
...or for ssh
git remote add origin git@github.com:KyleWashington73/wfb.git
git branch -M main
git push -u origin main
------------------------------------------------------------------------------------------------------------------------------
               **Let's Make a Basic Layout!**
// TITLE

# Dinosaurs

// MAIN CONTENT HERE

## About dinosaurs

### Their history

Dinosaurs are a diverse group of reptiles of the clade Dinosauria. 

[IMAGE HERE]

They first appeared during the Triassic period, between 243 and 233.23 million years ago, although the exact origin and timing of the evolution of dinosaurs is the subject of active research.

They became the dominant terrestrial vertebrates after the Triassic–Jurassic extinction event 201 million years ago; their dominance continued through the Jurassic and Cretaceous periods. Reverse genetic engineering and the fossil record both demonstrate that birds are modern feathered dinosaurs, having evolved from earlier theropods during the late Jurassic Period.

As such, birds were the only dinosaur lineage to survive the Cretaceous–Paleogene extinction event 66 million years ago. Dinosaurs can therefore be divided into avian dinosaurs, or birds; and non-avian dinosaurs, which are all dinosaurs other than birds. This article deals primarily with non-avian dinosaurs.

### People love dinosaurs!

Since the first dinosaur fossils were recognized in the early 19th century, mounted fossil dinosaur skeletons have been major attractions at museums around the world, and dinosaurs have become an enduring part of world culture.

The large sizes of some dinosaur groups, as well as their seemingly monstrous and fantastic nature, have ensured dinosaurs' regular appearance in best-selling books and films, such as Jurassic Park.

Persistent public enthusiasm for the animals has resulted in significant funding for dinosaur science, and new discoveries are regularly covered by the media.



// FOOTER

"There's an incomparable rush that comes from finding dinosaur bones. You know you're the first person to lay hands on a critter that lived 80 or 90 million years ago."

- Jack Horner

---------------------------------------------------------------
                     **Basic Layout**
*centering an on the page. 
  - Margins accept a set width, but you can also use the auto keyword.
  - Auto will automatically place all the available space on that side.
  - If we use auto on both the left and the right, it will center the element on the page.
---------------------------------------------------------------
                    **Creating Columns**
For the longest time we had to use something called floats to make block level elements go next to one another.
It involved things sliding under each other and clears. It was not fun.
Then we finally got flexbox. It was our first layout tool.
By default, when setting display: flex on a element, all the children will become columns.
---------------------------------------------------------------
                    **Creating a Layout!**
<html>
    <head>
        <title>HTML & CSS</title>
        <link href="css/style.css" rel="stylesheet">
    </head>
    <body>
     
     <header>
         <h1>I'm learning HTML and CSS</h1>
     </header>
     
     <main>
         <div class="intro">
             <h2>HTML and CSS are the building blocks of the web</h2>
             <p>Magna fringilla urna porttitor rhoncus dolor purus. Malesuada bibendum arcu vitae elementum. Purus sit amet volutpat consequat. </p>
         </div>
         
         <div class="my-skills">
             <div class="columns">
                 
                 <!-- column 1 -->
                 <div class="column">
                     <h3>HTML</h3>
                     <p>Magna fringilla urna porttitor rhoncus dolor purus. Malesuada bibendum arcu vitae elementum. Purus sit amet volutpat consequat. </p>
                 </div>
                 
                 <!-- column 3 -->
                 <div class="column">
                     <h3>CSS</h3>
                     <p>Magna fringilla urna porttitor rhoncus dolor purus. Malesuada bibendum arcu vitae elementum. Purus sit amet volutpat consequat. </p>
                 </div>
                 
                 <!-- column 3 -->
                 <div class="column">
                     <h3>And More</h3>
                     <p>Magna fringilla urna porttitor rhoncus dolor purus. Malesuada bibendum arcu vitae elementum. Purus sit amet volutpat consequat. </p>
                 </div>
                 
             </div> <!-- / columns -->
         </div> <!-- / my-skills -->
         
     </main>
     
    </body>
</html>


<!--
    Magna fringilla urna porttitor rhoncus dolor purus. Malesuada bibendum arcu vitae elementum. Purus sit amet volutpat consequat. 
-->
---------------------------------------------------------------
<html>
    <head></head>
    <body>
        <h1>⭐️ Gold star for you!<h1>
    </body>
</html>
---------------------------------------------------------------
                    **Flexbox Navbar**
<html>
    <head>
        <link rel="stylesheet" href="basic.css">
        <link rel="stylesheet" href="index.css">
    </head>
    <body>
        <nav>
            <ul class="container">
                <li>Home</li>
                <li>Profile</li>
                <li class="search">
                    <input type="text" class="search-input" placeholder="Search">
                </li>
                <li>Logout</li>
            </ul>
        </nav>
    </body>
</html>
-      -        -        -        -        -      -         -
                      **Basic CSS**
.container > li {
  padding: 10px;
  text-align: center;
  font-size: 2em;
  color: #ffeead;
  box-sizing: border-box;
  background-color: #96ceb4;
  list-style-type: none;
}

html, body {
  background-color: #ffeead;
  margin: 10px;
}

.container {
  padding: 0;
}
.search-input {
  background: #ff6e68;
  border: 0;
  width: 100%;
  outline: 0;
  background: transparent;
  border-bottom: 1px solid #ffeead;
  color: #ffeead;
}
::placeholder{
  color: #ffeead;
}

.search-input:focus {
  outline: none;
}

.container > li {
  background-color: #96ceb4;
}


/*.container > div:nth-child(2) {
  background-color: #ff6f69;
}

.container > div:nth-child(3) {
  background-color: #88d8b0;
}

.container > div:nth-child(4) {
  background-color: #96ceb4;
}
*/
-        -         -         -          -         -         -
                      **Index CSS**
.container {
  border: 5px solid #ffcc5c;
  display: flex;
}

.search {
  flex: 1;
}
-      -       -        -         -        -         -       -
                     **Index CSS #2**
.container {
  border: 5px solid #ffcc5c;
  display: flex;
}

.search {
  flex: 1;
}

@media all and (max-width: 600px) {
  .container {
    flex-wrap: wrap;
  }
  .container > li {
    flex: 1 1 50%;
  }
  .search > input {
    text-align: center;
  }
}
-       -        -          -          -           -       -   
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------
                                 **CSS GRID**
                                 *Basic HTML*
<html>
    <head>
        <link rel="stylesheet" href="basic.css">
        <style>
        </style>
    </head>
    <body>
        <div class="container">
            <div>1</div>
            <div>2</div>
            <div>3</div>
            <div>4</div>
            <div>5</div>
            <div>6</div>
        </div>
    </body>
</html>
                                 **CSS GRID**
                                 *Basic CSS*
.container > div {
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 2em;
    color: #ffeead;
}

html, body {
  background-color: #ffeead;
  margin: 10px;
}

.container > div:nth-child(1n) {
  background-color: #96ceb4;	
}

.container > div:nth-child(3n) {
  background-color: #88d8b0;
}

.container > div:nth-child(2n) {
      background-color: #ff6f69;
}

.container > div:nth-child(4n) {
      background-color: #ffcc5c;
}
----------------------------------------------------------------------------------------
                            **Fraction units and repeat**
                                    *Basic HTML*
<html>
    <head>
        <link rel="stylesheet" href="index.css">
        <link rel="stylesheet" href="basic.css">
    </head>
    <body>
        <div class="container">
            <div>1</div>
            <div>2</div>
            <div>3</div>
            <div>4</div>
            <div>5</div>
            <div>6</div>
        </div>
    </body>
</html>
----------------------------------------------------------------------------------------
                              **Fraction units and repeat**
                                      *Basic CSS*
     (You can use this layout for page 3 in the Clone Challenge!!!) 

.container > div {
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 2em;
    color: #ffeead;
}

html, body {
  background-color: #ffeead;
  margin: 10px;
}

.container > div:nth-child(1n) {
  background-color: #96ceb4;
	
}

.container > div:nth-child(3n) {
  background-color: #88d8b0;
}

.container > div:nth-child(2n) {
      background-color: #ff6f69;
}

.container > div:nth-child(4n) {
      background-color: #ffcc5c;
}
---------------------------------------------------------------------------------------
________________________________________________________________________________________
                             **Positioning items**
                                  *HTML*
<html>
    <head>
        <link rel="stylesheet" href="index.css">
        <link rel="stylesheet" href="basic.css">
    </head>
    <body>
        <div class="container">
            <div class="header">HEADER</div>
            <div class="menu">MENU</div>
            <div class="content">CONTENT</div>
            <div class="footer">FOOTER</div>
        </div>
    </body>
</html>                                 
----------------------------------------------------------------------------------------                            **Positioning items**
                                  *CSS*                
 .container {
    display: grid;
    grid-gap: 3px;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: 40px 200px 40px;
}

.header {
    grid-column: 2 / -1;
}

.menu {
    grid-row: 1 / 3;
}

.content {
    grid-column: 2 / -1;
}

.footer {
    grid-column: 1 / -1;
}
-----------------          --------------------            --------------          -----
________________________________________________________________________________________
                                **Template Areas**
                                   *Basic CSS*
.container {
    height: 100%;
    display: grid;
    grid-gap: 3px;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: 40px auto 40px;
}

.header {
    grid-column: 1 / -1;
}

.menu {}

.content {
    grid-column: 2 / -1;
}

.footer {
    grid-column: 1 / -1;
-_--------     -      -    -       -       -        -              -            - --   
                                 *Basic HTML*
<html>
    <head>
        <link rel="stylesheet" href="index.css">
        <link rel="stylesheet" href="basic.css">
    </head>
    <body>
        <div class="container">
            <div class="header">HEADER</div>
            <div class="menu">MENU</div>
            <div class="content">CONTENT</div>
            <div class="footer">FOOTER</div>
        </div>
    </body>
</html>
-        -          -          -          -           -          -           -         -
            **Method #2**   Use this for the Replica Challenge!!!  
                                *CSS*
.container {
    height: 100%;
    display: grid;
    grid-gap: 3px;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: 40px auto 40px;
    grid-template-areas: 
        "m h h h h h h h h h h h"
        "m c c c c c c c c c c c"
        "m f f f f f f f f f f f";
}

.header {
    grid-area: h;
}

.menu {
    grid-area: m;
}

.content {
    grid-area: c;
}

.footer {
    grid-area: f;
}
-         -          -         -              -         -        -             -       -
                                    *HTML*
html>
    <head>
        <link rel="stylesheet" href="index.css">
        <link rel="stylesheet" href="basic.css">
    </head>
    <body>
        <div class="container">
            <div class="header">HEADER</div>
            <div class="menu">MENU</div>
            <div class="content">CONTENT</div>
            <div class="footer">FOOTER</div>
        </div>
    </body>
</html>
-          --            -        -      -         -        -          -           -   -
                                  *Implicit*
.container {
    display: grid;
    grid-gap: 5px;
    grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
    grid-auto-rows: 100px;
}
-             -         -           -           -          -           -          -     
                        **An Awesome Image Grid!!!**
                                *HTML*
 <html>
    <head>
        <link rel="stylesheet" href="index.css">
        <link rel="stylesheet" href="basic.css">
    </head>
    <body>
        <div class="container">
            <div><img src="img/normal1.jpg"/></div>
            <div class="vertical"><img src="img/vertical1.jpg"/></div>
            <div class="horizontal"><img src="img/horizontal1.jpg"/></div>
            <div><img src="img/normal2.jpg"/></div>
            <div><img src="img/normal3.jpg"/></div>
            <div class="big"><img src="img/big1.jpg"/></div>
            <div><img src="img/normal4.jpg"/></div>
            <div class="vertical"><img src="img/vertical2.jpg"/></div>
            <div><img src="img/normal5.jpg"/></div>
            <div class="horizontal"><img src="img/horizontal2.jpg"/></div>
            <div><img src="img/normal6.jpg"/></div>
            <div class="big"><img src="img/big2.jpg"/></div>
            <div><img src="img/normal7.jpg"/></div>
            <div class="horizontal"><img src="img/horizontal3.jpg"/></div>
            <div><img src="img/normal8.jpg"/></div>
            <div class="big"><img src="img/big3.jpg"/></div>
            <div><img src="img/normal9.jpg"/></div>
            <div class="vertical"><img src="img/vertical3.jpg"/></div>
        </div>
    </body>
</html>                               
-        -        -        -         -          -          -         -        -        -
                                       *Basic CSS*
.container > div {
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 2em;
    color: #ffeead;
}

.container > div > img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

html, body {
    background-color: #ffeead;
    margin: 10px;
}
-      -       -         -          -         -         -           -         -        -
                                   *Index CSS*
.container {
    display: grid;
    grid-gap: 5px;
    grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
    grid-auto-rows: 75px;
}

.horizontal {}

.vertical {}

.big {}
-       -        -         -         -          -        -          -           -      
.container {
    display: grid;
    grid-gap: 5px;
    grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
    grid-auto-rows: 75px;
}

.horizontal {
    grid-column: span 2;
}

.vertical {}

.big {}
-       -        -          -           -        -           -          -         -    -
.container {
    display: grid;
    grid-gap: 5px;
    grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
    grid-auto-rows: 75px;
}

.horizontal {
    grid-column: span 2;
}

.vertical {
    grid-row: span 2;
}

.big {}
-        -          -         -          -          -           -           -         -
.container {
    display: grid;
    grid-gap: 5px;
    grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
    grid-auto-rows: 75px;
    grid-auto-flow: dense;
}

.horizontal {
    grid-column: span 2;
}

.vertical {
    grid-row: span 2;
}

.big {
    grid-column: span 2;
    grid-row: span 2;
}
-        -          -          -           -          -        -         -          -  
________________________________________________________________________________________
                                  **Named Lines**   
.container {
    display: grid;
    grid-gap: 5px;
    grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
    grid-auto-rows: 75px;
    grid-auto-flow: dense;
}

.horizontal {
    grid-column: span 2;
}

.vertical {
    grid-row: span 2;
}

.big {
    grid-column: span 2;
    grid-row: span 2;
}
-         -          -         -         -        -         -          -          -    
                              *Basic*
.container > div {
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 2em;
    color: #ffeead;
}

html, body {
    box-sizing: border-box;
    background-color: #ffeead;
    height: 100%;
    padding: 10px;
    margin: 0px;
}

.container > div:nth-child(1n) {
    background-color: #96ceb4;	
}

.container > div:nth-child(3n) {
    background-color: #88d8b0;
}

.container > div:nth-child(2n) {
    background-color: #ff6f69;
}

.container > div:nth-child(4n) {
    background-color: #ffcc5c;
}
-        -        -          -          -         -        -           -           -  
<html>
    <head>
        <link rel="stylesheet" href="index.css">
        <link rel="stylesheet" href="basic.css">
    </head>
    <body>
        <div class="container">
            <div class="header">HEADER</div>
            <div class="menu">MENU</div>
            <div class="content">CONTENT</div>
            <div class="footer">FOOTER</div>
        </div>
    </body>
</html>
-        -         -          -         -           -          -          -          -  
                            **Justify/Align Content**
*justify-content:  start, center, end, space-between, space-evenly, space-around.
*align-content: start, center, end, space-between, space-evenly, space-around. 
________________________________________________________________________________________
                           **Justify/Align Items**
*justify-items: start; stretch; end;
*Align-items: start; center; end; 
*You can use both of them together to manipulate code...
    for example:         
    
     .container {
    height: 100%; 
    display: grid;
    grid-gap: 3px;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: 40px auto 40px;
    justify-items: center;
    align-items: center;
}

.header {
    grid-column: 1 / -1;
}

.menu {
    grid-column: 1 / 3;
}

.content {
    grid-column: 3 / -1;
}

.footer {
    grid-column: 1 / -1;
}


also...          justify-self: center;

_______________________________________________________________________________________
                           **Auto-fit vs. Auto-fill**             
.container {
    border: 1px solid black;
    display: grid;
    grid-gap: 5px;
    grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
    grid-template-rows: 100px 100px;
}

.container2 {
    border: 1px solid black;
    display: grid;
    grid-gap: 5px;
    grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
    grid-template-rows: 100px 100px;
}
_______________________________________________________________________________________
                            **Creating an Article Layout**
???????????????????????????????????????????????????????????????????????????????????????

_______________________________________________________________________________________
                               **Grid vs. Flexbox**
<html>
    <head>
        <link rel="stylesheet" href="basic.css">
        <link rel="stylesheet" href="index.css">
    </head>
    <body>
        <p>FLEXBOX HEADER</p>
        <div class="flexbox-header">
            <div>HOME</div>
            <div>SEARCH</div>
            <div>LOGOUT</div>
        </div>
        <br>
        <p>GRID PAGE</p>
        <div class="grid-page">
            <div class="header">HEADER</div>
            <div class="menu">MENU</div>
            <div class="content">CONTENT</div>
            <div class="footer">FOOTER</div>
        </div>
    </body>
</html>
 --   -      -     -         -       -      -      -        -     -       -     -     
.flexbox-header {
    display: flex;
}

.flexbox-header > div:nth-child(3) {
    margin-left: auto;
}

.grid-page {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: 40px 200px 40px;
}

.header {
    grid-column: 1 / -1;
}

.menu {
    grid-column: 1 / 2;
}

.content {
    grid-column: 2 / -1;
}

.footer {
    grid-column: 1 / -1;
}
-           -             -            -             -           -           -       - 
                                       *Basic CSS*
html, body {
  background-color: #ffeead;
  margin: 10px;
  font-size: 20px;
}

p {
  color: #96ceb4;
  text-align: center;
}

.flexbox-header > div {
  display: flex;
  font-size: 1em;
  padding: 10px 20px;
}

.flexbox-header {
  background-color: #96ceb4;
  color: #ffeead;
}


.header {
    background-color: #96ceb4;	
}

.header :nth-child(2) {
    padding: 0 40px;
}

.menu {
    background-color: #ff6f69;
}

.content {
    background-color: #ffcc5c;
}

.footer {
    background-color: #88d8b0;
}

.grid-page > div {
    color: #ffeead;
    display: flex;
    align-items: center;
    padding: 0px 20px;
}
** Flexbox is built for 1 dimensional layouts!
** CSS Grid is built for 2 dimensional layouts!

** Flexbox is content first!
** CSS Grid is layout first!
______________________________________________________________
                    **Page #3**
 <div class="page-3">
                <div class="container">
                    <div>1<img src="./img/hawkeye.jpg" alt=""></div>
                    <div>2<img src="./img/encanto.jpg" alt=""></div>
                    <div>3<img src="./img/eternals.jpg" alt=""></div>
                    <div>4<img src="./img/boba-fett.jpg" alt=""></div>
                    <div>5<img src="./img/beetles.jpg" alt=""></div>
                    <div>6<img src="./img/simpsons.jpg" alt=""></div>
                    <div>7<img src="./img/raya.jpg" alt=""></div>
                    <div>8<img src="./img/soul.jpg" alt=""></div>
                    <div>9<img src="./img/will-smith.jpg" alt=""></div>   
                </div>
        </div>
-    -    -    -    -    -   -    -    -   -      -   -   - 
                            **Page#3 CSS**
.container > div {
    align-items: center;
    font-size: 2em;
    color: #ffeead;
}

html, body {
  background-color: #ffeead;
  margin: 10px;
}

.container > div:nth-child(1n) {
  background-color: #96ceb4;	
}

.container > div:nth-child(3n) {
  background-color: #88d8b0;
  display: grid;
  grid-template-columns: 100px auto 100px;
  grid-template-rows: 50px 50px;
}

.container > div:nth-child(2n) {
      background-color: #ff6f69;
}

.container > div:nth-child(4n) {
      background-color: #ffcc5c;
}
______________________________________________________________

<div class="page-4-cotainer"><p style="color: lightgray; font: 1.3em sans-serif;">Get The Disney Bundle to stream the best movies,<br>shows, and sports with Disney+, Hulu, and ESPN+. <u style="color: aliceblue;">Terms<br> Apply.</u> Learn more about <u style="color: aliceblue;"> Disney Bundle.</u> </div></p>
        <div><img src="./img/page-4-logo.jpg" alt=""></div>
        

                   **page4**
<div class="card mb-3 bg-dark mb-3" style="max-width: fit-content max-height: fit-content; font: 1em sans-serif; padding: 5em;">
                <div class="row g-0">
                  <div class="col-md-8">
                    <img src="./img/page-4-logo.jpg" class="img-fluid rounded-start" alt="...">
                  </div>
                  <div class="col-md-4">
                    <div class="card-body max-height 100% bg-dark mb-3" style="color: black;"> 
                      <h5 class="card-title"></h5>
                      <p class="card-text" style="color: lightgrey; font: 1.1em sans-serif;">Get The Disney Bundle to stream the best movies,<br>shows, and sports with Disney+, Hulu, and ESPN+. <u style="color: aliceblue;">Terms<br> Apply.</u> Learn more about <u style="color: aliceblue;"> Disney Bundle.</u> </div></p>
                      <p class="card-text"><small class="text-muted" style="color: black;"> </small></p>
                      <div class="d-grid gap-2 1d-md-block">
                      <button type="button" class="btn btn-primary btn-lg">SIGN UP NOW</button>
                    </div>
                    </div>
                  </div>
                </div> 
              </div>






color d-md-block mb-3


  <script src="./js/script.js"></script>


<script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.9.2/dist/umd/popper.min.js" integrity="sha384-IQsoLXl5PILFhosVNubq5LC7Qb9DXgDA9i+tQ8Zj3iwWAwPtgFTxbJ8NT4GN1R8p" crossorigin="anonymous"></script>
    <script src="js/bootstrap.js"></script>
    <script src="./js/script.js"></script>


<link rel="stylesheet" href="css/bootstrap.css">





<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">
    <title>Replica Challenge - Disney+</title>
    <link rel="stylesheet" href="css/style.css">
    <link rel="stylesheet" href="index.css">
    <link rel="stylesheet" href="basic.css">
    
</head>
<body>
    <div class="container">
        <div class="page-1">
            <!-- Header -->
            <div class="page-1-main">
                <img src="./img/page-1-logos-top.svg" alt="Main">
                <button>GET THE DISNEY BUNDLE</button>
                <p>Stream now. <a href="#">Terms Apply</a></p>
                <img src="./img/page-1-logos.png" alt="Bottom">
                <a href="#">Sign up for Disney+ only</a>
            </div>
        </div>
        <div class="page-2">
            <img src="./img/page-2-img.png" alt="">
            <ul class="page-2-text">
                <h1>Watch the way you want</h1>
                <li>Host virtual movie nights with GroupWatch. Pause, rewind and react with up to six friends. Subscription is required to join GroupWatch.</li>
                <li>Download any more or series and watch on-the-go.</li>
                <li>Enjoy an ever-growing range of titles in stunning 4k UHD and Dulby Atmos sound on compatible devices.</li>
                <li>Stream on up to four devices at the same time.</li>
            </ul>
        </div>
        <div class="page-3">
            <ul>
                <h2>Disney+ has your favorite stories</h2>
                <p>An unprecedented collection of the world's most beloved movies and TV series.</p>
            </ul>    
            <div class="page-3-container">
                <div><img src="./img/hawkeye.jpg" alt=""></div>
                <div><img src="./img/encanto.jpg" alt=""></div>
                <div><img src="./img/eternals.jpg" alt=""></div>
                <div><img src="./img/boba-fett.jpg" alt=""></div> 
                <div><img src="./img/beetles.jpg" alt=""></div>
                <div><img src="./img/simpsons.jpg" alt=""></div>
                <div><img src="./img/raya.jpg" alt=""></div>
                <div><img src="./img/soul.jpg" alt=""></div>
                <div><img src="./img/will-smith.jpg" alt=""></div>   
            </div>
        </div>

        <!-- Page 4 -->
        <section class="border">
            <div class="card" style="max-width: fit-content; max-height:max-content fit-content; font:  1em sans-serif; padding: 5em; background: #000;">
                <div class="row g-0">
                  <div class="col-md-8">
                    <img src="./img/page-4-logo.jpg" class="img-fluid rounded-start" alt="...">
                  </div> 
                  <div class="col-md-4">
                    <div class="card-body max-height 100% bg-dark "> 
                      <h5 class="card-title"></h5 >
                      <p class="card-text" style="color: gray; font: 1.1em sans-serif 1em sans-serif; background: #000; ">Get The Disney Bundle to stream the best movies,<br>shows, and sports with Disney+, Hulu, and ESPN+. <u style="color: aliceblue;">Terms<br> Apply.</u> Learn more about <u style="color: aliceblue;"> Disney Bundle.</u> </div></p>
                      <p class="card-text"><small class="text-muted"> </small></p>
                      <div class="d-grid gap-2 1d-md-block">
                      <button type="button" class="btn btn-primary btn-lg font: .4em sans-serif;">SIGN UP NOW</button>
                    </div>
                    </div>
                  </div>
                </div> 
              </div>
        </section>
       <!-- Page 4 end -->
       
        <!-- </div> -->
        <div class="page-5-container">
              </div>  
        </div>  
        <div class="page-6">  
        </div>
        <div class="page-7">
            <!-- Footer -->
        </div>
    </div>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.bundle.min.js" integrity="sha384-MrcW6ZMFYlzcLA8Nl+NtUVF0sA7MsXsP1UyJoMp4YLEuNSfAP+JcXn/tWtIaxVXM" crossorigin="anonymous"></script>   
</body>
</html>


@font-face {
    font-family: "Avenir";
    src: url("../fonts/AvenirLTStd-Black.otf");
}

body {
    /* background-color: #040714; */
    margin: 0px;
    padding: 0px;
    height: 100%;
    width: 100%;
    font-family: "Avenir", sans-serif;
}



/* Page 1 */

.page-1 {
    width: 100%;
    height: 100vh;
    /* border: 1px solid #fff; */
    background-image: url("../img/page-1-bg.jfif");
    background-size: 100% 110vh;
    background-repeat: no-repeat;

    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

.page-1-main {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 50%;
    /* height: inherit; */
}

.page-1-main img {
    width: 75%;
    margin: 5px;
}

.page-1-main > button {
    width: 75%;
    height: 3rem;
    background-color: #0063e5;
    border: none;
    border-radius: 5px;
    color: #f9f9f9;
    text-align: center;
    cursor: pointer;
    padding: 5px;
    margin: 5px;
}

.page-1-main > p,
.page-1-main > a {
    margin: 5px;
    padding: 5px;
    color: #fff;
}

/* Page 2 */
.page-2 {
    height: 100vh;
    /* border: 1px solid #fff; */
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    padding: 1rem;
}

.page-2-text {
    display: flex;
    flex-direction: column;
    /* justify-content: flex-start; */
    align-items: flex-start;
    color: #fff;
    width: auto;
    margin-left: 3rem;
    padding: 1rem;
}

.page-2-text h1 {
    margin-left: -2rem;
}

.page-2-text > li {
    line-height: 30px;
}

/* Page 3 */

.page-3 {
    color: #fff;
    border: 1px solid black;
}

.page-3> ul > h2 {
     text-align:center;
     font-size: 30px;
}

.page-3> ul > p {
    text-align:center;
    font-size: px;
    color:#bfbfbf;
    font: 1em sans-serif;
}

.page-3-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
    margin-bottom: 05em;
}

.page-3-container > div {
    font-size: 2em;
    color: white;
}

.page-3-container > div > img {
    width: 378px;
    height: 227px;
    object-fit: cover;
    margin: 1rem;
}

html, body {
    background-color: #080703;
    margin: 0px;
}

/* Banner/Page 4 */
 .border {
    column-count: 2;
    flex-direction: column;
    display: flex;
    height: 415px;
    padding: 0em;
}

.page-4 {
    color: #08010800;
    width: 100%;
    height: 5vh;
}

.page-4-container > div > img {
    display: flex ;
    justify-content: flex;
    border: 1px solid rgb(8, 0, 0);
    margin: 0rem;
    vertical-align:center;
    height 100%;
    color: #000;
}

.page-4-container {
    text-align: right;
    height: 50px;
    margin-top: 7em;
    
}

.bg-dark {
    background-color: #212529!important;
    flex: 1 1 auto;
    padding: 0rem 0rem;
}

    
/* Page 5 */

.page-5 {
    width: 100%;
    height: 100vh;
    border: 1px solid #fff;
}

.page-5-container {
    margin-top: 10em;
}

/* Page 6 */

.page-6 {
    width: 100%;
    height: 130vh;
    border: 1px solid #fff;
}

/* Page 7 */

.page-7 {
    width: 100%;
    height: 40vh;
    border: 1px solid #fff;
}


new clone project
git push --set-upstream origin navbar


4 git branch -r
   5 git checkout -b header
   6 git switch main
   7 git add .
   8 git commit -m "initial commit"
   9 git push
  10 git switch header
  11 git pull origin main



 <img src="./IMG/header-photo.jpg" alt="">


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="CSS/style.css">
   
    <title>header section</title>
    <!-- stylesheet -->
    <style>
        body {
            background-image: url('./IMG/header-photo.jpg');
            background-repeat: no-repeat;
            height: 100%;
            width: 100%;
        }
    </style>

</head>

<body>

<!-- NAVBAR -->    
<menu>
    <li>logo</li>
    <li>search</li>
</menu>

<!-- HEADER  -->
<div class="header-container">
    <h1 style="color: white;">Architectural Design</h1>
    <p  style="color: silver;">We are an independent firm of designers, engineers, architects,<br> planners, consultants and technical specialists</p>
</div>















    
</body>
</html>
 




body {
    background-color: rgb(252, 249, 249);
    width: 100%;
    height: 100%;
    margin: 0em;
    padding: 0em;
    font-family: "Avenir", sans-serif;
}

.header-container > img > p {
    background-image: url('./IMG/header-photo.jpg');
    text-align: center;
}


<!-- Image source -->
<img src="CSS/style.css/IMG/header-photo.jpg" alt="Snow" style="width:100%;">

<!-- Image Tag -->
<div class="container" >
        <img src="./IMG/header-photo.jpg" alt="" >
    </div>

 <!-- MAIN SECTION 1 -->
   <div class="main-container">
    <div class="row-big-main-container"><img src="./IMG/main-photo1.jpg" alt="main" style="width: 550px; height: 550px; margin-right: 20px; margin-bottom: 90px;"></div>
    <div class="row-small-main-container"><img src="./IMG/main-photo4.jpg" alt="main" style="width: 200px; height: 300px; margin-bottom: 247px;"></div>
    <div class="row-small-main-container"><img src="./IMG/main-photo5.jpg" alt="main" style="width: 200px; height: 300px; margin:20px; margin-bottom: 260px;"></div><br>
   </div>
    <!-- MAIN SECTION 2 -->
   <div class="main-container2"> 
    <div class="row-small-main-container"><img src="./IMG/main-photo2.jpg" alt="main" style="width: 200px; height: 300px; margin: 20px; margin-top: 100%; margin-left: 0px;"></div>
    <div class="row-small-main-container"><img src="./IMG/main-photo3.jpg" alt="main" style="width: 200px; height: 300px; margin-top: 100%; margin-left: 0px;"></div>
    <div class="row-big-main-container"><img src="./IMG/main-photo6.jpg" alt="main" style="width: 550px; height: 550px; margin-left: 250px;"></div>
   </div>
____________________________________________________________________________________________
              **PHP**
<?php
print "Hello, World!\n";
?>

<?php
print "Hello, World!\n";
?>


C-Style printf
printf("%s\n", "Hello, World!");
?>

     *PHP opening tag*

<?php>

-Can function without closing tag.

-Statements in PHP must be terminated with a semicolon.

-It is not required to use parentheses with the echo function.

-Boolean#
This is the simplest data type with only two possible values, i.e., true and false. 
<?php
$foo = true;
$bar = false;
?>

-An integer is a positive or negative number.
<?php
$negative = -3; // negative
$zero = 0; // zero (can also be null or false (as boolean)
$positive = 123; // positive decimal
$zeroPos = 0123; //0 prefix is used to specify octal - octal value = 83 decimal
$hex = 0xAB; //0x prefix is used to specify hexadecimal - hexadecimal value = 171 decimal
$bin = 0b1010; // 0b prefix is used to specify binary - binary value = 10 decimal
var_dump($negative, $zero, $positive, $zeroPos, $hex, $bin); 
?>

-Floating point numbers, “doubles” or simply called “floats” are decimal numbers.
<?php
$foo1 = 1.23;
$foo2 = 10.0;
$bar1 = -INF; // -INF refers to negative infinity
$bar2 = NAN; // NAN stands for 'Not a Number'
var_dump($foo1,$foo2,$bar1,$bar2);
?>

-An array is like a list of values. The simplest form of an array is indexed by an integer, and ordered by the index, with the first element lying at index 0
<?php
$foo = array(1, 2, 3); // An array of integers created using array fucntion
$bar = ["A", true, 123 => 5]; // Short array syntax, PHP 5.4+
echo $bar[0]; // Returns "A"
echo "\n";
echo $bar[1]; // Returns 1 for true
echo "\n";
echo $bar[123]; // Returns 5
// echo $bar[1234]; // uncommenting this line will give an error because 1234 is inaccessable
?>

-Arrays can also associate a key other than an integer index to a value. In PHP, all arrays are associative arrays behind the scenes, but when we refer to an associative array explicitly, we usually mean one that contains one or more keys that aren’t integers.
<?php
$array = array();
$array["foo"] = "bar";
$array["bar"] = "quux";
$array[42] = "hello";
echo $array["foo"]; // Outputs "bar"
echo "\n";
echo $array["bar"]; // Outputs "quux"
echo "\n";
echo $array[42]; // Outputs "hello"
?>

-A string is like an array of characters. Like an array, a string can be indexed to return its individual characters:
<?php
$foo = "I am a string";
echo $foo; // outputs "I am a string"
echo "\n";
echo $foo[3]; // Prints 'm', the third character of the string in $foo.
?>

-Using PHP, we can access data through dynamic variable names. The name of a variable can be stored in another variable, allowing it to be accessed dynamically. Such variables are known as variable variables.

To turn a variable into a variable variable, you put an extra $ sign in front of your variable. This method is illustrated in the following figure:

Using {} is only mandatory when the name of the variable is itself an expression, like this:
<?php
${$variableNamePart1 . $variableNamePart2} = $value;
?>

It is nevertheless recommended to always use {} because it’s more readable.

-Constants, by definition, are variables that cannot be modified during the execution of the script. They are created using the const statement or the define function.
Convention: In PHP, the convention is to use uppercase letters for constant names, e.g., A_CONSTANT.
<?php
const PI = 3.14; // float
define("EARTH_IS_FLAT", false); // boolean
const UNKNOWN = null; // null
define("APP_ENV", "dev"); // string
const MAX_SESSION_TIME = 60 * 60; // integer, using (scalar) expressions is ok
const APP_LANGUAGES = ["de", "en"]; // arrays
define("BETTER_APP_LANGUAGES", ["lu", "de"]); // arrays
?>
f you have already defined one constant, you can define another one based on it:
<?php
const TAU = PI * 2;
define("EARTH_IS_ROUND", !EARTH_IS_FLAT);
define("MORE_UNKNOWN", UNKNOWN);
define("APP_ENV_UPPERCASE", strtoupper(APP_ENV)); // string manipulation is ok too
define("MAX_SESSION_TIME_IN_MINUTES", MAX_SESSION_TIME / 60);
const APP_FUTURE_LANGUAGES = [-1 => "es"] + APP_LANGUAGES; // array manipulations
define("APP_BETTER_FUTURE_LANGUAGES", array_merge(["fr"],BETTER_APP_LANGUAGES));
?>
Note: Remember that you can not use a constant for a function call like this:

-An operator is something that takes one or more values (or expressions, in programming jargon) and yields another value (so that the construction itself becomes an expression). For instance, when you add two numbers, say 2 and 5 (values) it yields 7 (value), such that the construction itself becomes an expression, i.e. 2+5=7.

-There are multiple types of operators for various purposes, i.e.,

-arithmetic operators
comparison operators
logical operators
assignment operators
The following figure illustrates the various kinds of operators in PHP:

-Arithmetic operators, as the name suggests, are used to perform basic arithmetic. They are further divided into types:

Binary Operators
Unary Operators

-Binary operators are the ones that take two values and perform an arithmetic operation on them.

-The following table discusses the various arithmetic operators and their functions:

Operator	Function	Example
+	Addition	\$a + \$b
-	Subtraction	\$a - \$b
*	Multiplication	\$a * \$b
/	Division	\$a / \$b
%	Modulus	\$a % \$b

-Unary operators are the type of arithmetic operators that perform arithmetic on only one value.

There are two unary operators:

Incrementing operator: ++
Decrementing operator: --
Variables can be incremented by 1 using the ++ operator and can be decremented by 1 using the operator --. They can either precede or succeed variables, resulting in different executions of the code. An example of this is shown below:

-Operator precedence determines which operator is performed first in an expression with more than one operators. Operator precedence in PHP is similar to that of regular arithmetic operators.
*, /, % operators have equal precedence.
+ , - operators have equal precedence.
*, / , % have a higher precedence than + , -.
The operator with higher precedence is executed first in the expression.

-Associativity is used when two operators of the same precedence appear in an expression.

-Associativity is used when two operators of the same precedence appear in an expression.
100 / 10 * 10 
is treated as:

(100 / 10) * 10

-Right Associativity #
Right associativity occurs when an expression is evaluated from right to left. Like most programming languages, = and print in PHP have right associativity.

Run the following code to see a few examples:

Remember: It is good to know precedence and associativity rules, but the best thing is to use brackets. Brackets increase readability of the code as the reader doesn’t have to see the table to find out the order.

-Comparison operators, as the name suggests, allow you to compare two values. The following table illustrates the different comparison operators in PHP:

Operator	Name	Example
==	Equal	a==b
===	Identical	a===b
!=	Not Equal	a!=b
!==	Not Identical	a!==b
<	Less than	a<b
>	Greater than	a>b
<=	Less than equal to	a<=b
>=	Greater than equal to	a>=b

-The spaceship operator (<=>) is a special kind of comparison operator. It

returns -1 if first expression is lesser than the second expression.
returns 1 if the first expression is greater than the second expression.
returns 0 if the first expression is equal to the second expressio

-Remember: Objects are not comparable, and doing so will result in undefined behavior.





Step1. Download VScode and exteentions. Download and install Vscode and from the microsoft website https://code.visualstudio.com/download. ...
Set up Code Runner with C++17 flag. Go to Code / Prefrences / Settings then Select Extensions -> Run Code Configure -> Executor Map.


                            *php site**
                         https://replit.com/ 




<div class="main-section">
   <!-- MAIN SECTION 1 -->
    <div class="photo1"><img src="./IMG/main-photo1.jpg" alt="main"></div>
    <div class="photo2"><img src="./IMG/main-photo4.jpg" alt="main"></div>
    <div class="photo3"><img src="./IMG/main-photo5.jpg" alt="main"></div><br>
    <!-- MAIN SECTION 2 --> 
    <div class="photo4"><img src="./IMG/main-photo6.jpg" alt="main"></div>
    <div class="photo5"><img src="./IMG/main-photo2.jpg" alt="main"></div>
    <div class="photo6"><img src="./IMG/main-photo3.jpg" alt="main"></div>
   </div>


.main-section {
  display: grid;
  grid-template-columns: repeat(2, 360px);
 
  grid-gap: 5px;
}

.photo1 {
  grid-column-start: 1/span 2;
  grid-column-end: 1 / span 2;
}

.photo2 {
  grid-row: 2 /span 3;
  grid-column: 2 / span -4;
}

.photo3 {
  grid-row: 3 / span 4;
  grid-column: 3 / span 2;
}

.photo4 {
  grid-row: 2 / span 3;
  grid-column: 2 / span 2;
}

.photo5 {
  grid-row: 3 / 4;
  grid-column: 3 / 2;
}

.photo6 {
  grid-row: 3 / -1;
  grid-column: 2 / 3;
}


The vertical lines of grid items are called columns.

The horizontal lines of grid items are called rows.

http://127.0.0.1:5501/index.html

yfranco@horstmannfis.com
Yulianna Franco
____________________________________________________________________________________________
PHP is a server-side programming language that will run on the server. A server is a machine that will store all of your files and information. After you save your files on the server, you can access and manage them for your needs. 

There is also a reason why you should use index.php and not index.html. The ending .php indicates that your files store PHP code. This way the interpreter will understand that it has to check the PHP part of the code before delivering it.

Keep in mind, that during this course, you will have to use both PHP and HTML programming languages.

HTML (HyperText Markup Language) is one of the basic languages that will allow you to build amazing websites. It is relatively easy to learn and is one of the most known programming languages.

However, you’ll also have the style.css tab available to you. This tab requires for you to write CSS code. The main function of CSS is to style your document and make it look neat! We do not emphasize CSS during this course, so it is OK if you are not familiar with it.

If you are completely new to coding, it would be very useful in this course if you checked out our gamified course called SpaceDoggos 2, where you can get familiar with CSS and HTML. 
____________________________________________________________________________________________

      ** My Cursor Keeps Jumping!!! **

-Right click the Windows Start button and select Settings.
-Select Devices and Mouse.
-Select Additional Mouse Options from the center.
-Select the Pointer Options tab in the new window.
-Uncheck the box next to Enhance Pointer Precision.
-Retest your mouse for a little while.
*Computer Cursor Keeps Jumping Around – What To Do
____________________________________________________________________________________________
<?php





$stringOne = 'my email is ';
$stringTwo= 'kylewash916@gmail.com';

// This is an example of a string.
echo $stringOne.$stringTwo;

?>

<!DOCTYPE html>
<html>
<head>
  <title>PHP Tutorials</title>
</head>
<body>


  
</body>
</html> 


media sass project: Kick Ass Grid System!!!
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="SASS/style.css">
    <title></title>
</head>
<body>
  <!-- First Body Container -->
<div class="grid-container-1">
    <img src="./img/cool-stang-photo.jpg" alt="">
</div>
  <!-- Second Body Container -->
<section class="border">
 <div class="grid-container-2">
   <div class="grid-item grid-item1"></div>
   <div class="grid-item grid-item2"><img src="./img/redr8.jpg" alt=""></div>
   <div class="grid-item grid-item3"><h1 class="h1">BEST CAR<br><p>SERVICE</p><br><p class="p">A regular service schedule can help <br><p class="p">keep your car running at it's best. A <br><p class="p">regular service schedule can help <br><p class="p">keep your car running at it's best  <br><button type="button" class="button">READ MORE</button></p></p></p></p></h1></div>
 </div>
</section>
<!-- Third Body Container --> 
<section class="border">
<div class="grid-container-3">
  <div class="grid-item grid-item4"><h2>RENTAL CAR SERVICES</h2><p>Find the best possible rental car<br>rate. Compare rates worldwide and save <br>up to 60% on deals from  over 1,053 car<br>rental companies.</p></div>
  <div class="grid-item grid-item5"><img src="./img/location-symbol.jpg" alt=""><p>LOCATION</p></div>
  <div class="grid-item grid-item6"><img src="./img/car-symbol.jpg" alt=""><p>250+ CARS</p></div>
  <div class="grid-item grid-item7"><img src="./img/family.jpg" alt=""><p>HAPPY<br> USERS</p></div>
</div>
</section>
<!-- Fourth Body Container -->
<div class="grid-container-4">
  <div class="grid-item-A grid-item-8">
    item 1
  </div>
  <div class="grid-item-A grid-item-9">
    item 2
  </div>
  <div class="grid-item-A grid-item-10">
    item 3
  </div>
  <div class="grid-item-A grid-item-11">
    item 4
  </div>
  <div class="grid-item-A grid-item-12">
    item 5
  </div>
  <div class="grid-item-A grid-item-13">
    item 6
  </div>
  <div class="grid-item-A grid-item-14">
    item 7
  </div>
  <div class="grid-item-A grid-item-15">
    item 8
  </div>
</div>

</body>
</html>


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="SASS/style.css">
    <title></title>
</head>
<body>
  <!-- First Body Container -->
<div class="grid-container-1">
    <img src="./img/cool-stang-photo.jpg" alt="">
</div>
  <!-- Second Body Container -->
<section class="border">
 <div class="grid-container-2">
   <div class="grid-item grid-item1"></div>
   <div class="grid-item grid-item2"><img src="./img/redr8.jpg" alt=""></div>
   <div class="grid-item grid-item3"><h1 class="h1">BEST CAR<br><p>SERVICE</p><br><p class="p">A regular service schedule can help <br><p class="p">keep your car running at it's best. A <br><p class="p">regular service schedule can help <br><p class="p">keep your car running at it's best  <br><button type="button" class="button">READ MORE</button></p></p></p></p></h1></div>
 </div>
</section>
<!-- Third Body Container --> 
<section class="border">
<div class="grid-container-3">
  <div class="grid-item grid-item4"><h2>RENTAL CAR SERVICES</h2><p>Find the best possible rental car<br>rate. Compare rates worldwide and save <br>up to 60% on deals from  over 1,053 car<br>rental companies.</p></div>
  <div class="grid-item grid-item5"><img src="./img/location-symbol.jpg" alt=""><p>LOCATION</p></div>
  <div class="grid-item grid-item6"><img src="./img/car-symbol.jpg" alt=""><p>250+ CARS</p></div>
  <div class="grid-item grid-item7"><img src="./img/family.jpg" alt=""><p>HAPPY<br> USERS</p></div>
</div>
</section>
<!-- Fourth Body Container -->
<div class="grid-container-4">
  <div class="grid-item-A grid-item-8">
    item 1
  </div>
  <div class="grid-item-A grid-item-9">
    item 2
  </div>
  <div class="grid-item-A grid-item-10">
    item 3
  </div>
  <div class="grid-item-A grid-item-11">
    item 4
  </div>
  <div class="grid-item-A grid-item-12">
    item 5
  </div>
  <div class="grid-item-A grid-item-13">
    item 6
  </div>
  <div class="grid-item-A grid-item-14">
    item 7
  </div>
  <div class="grid-item-A grid-item-15">
    item 8
  </div>
</div>

</body>
</html>

body {
    background-color: white;
}



* { 
    margin: 0px;
    padding:0px;
    box-sizing: content-box;
    font-size: 30px;
}
// Container 1 //
.grid-container-1 > img {
width: 45em;       
}
// Container 2 //
.grid-container-2 {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr;
    grid-template-rows: 1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr;
    height: 700px;
    width: 30em;
    margin-left: 50px;
    margin-top: 200px;
    border: 0px solid white;
    background-color: white; 
}

.grid-item {
    background-color: rgb(14, 13, 13);
    border: 0px solid white;
    padding: 0px;
}

.grid-item1 {
    grid-column-start: 1;
    grid-column-end: 7;
    grid-row-start: 1;
    grid-row-end: 6;
    background-color: rgb(14, 13, 13);

}

.grid-item2 {
    grid-column-start: 2;
    grid-column-end: 6;
    grid-row-start: 2;
    grid-row-end: 5;
    background-color: rgb(14, 13, 13);
}

.grid-item3 {
   grid-column-start: 7;
   grid-column-end: 8;
   grid-row-start: 2;
   grid-row-end: 5;
   background-color: white;

} 

.button {
   background-color: #0c0f0d; /* Black */
   border: none;
   color: white;
   padding: 15px 32px;
   text-align: center;
   text-decoration: none;
   display: inline-block;
   font-size: 22px;
   margin-top: 20px;
   height: 60px;
   width: 245px;
 
}

  // Container 3 // 
.grid-container-3 {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr;
    grid-template-rows: 1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr;
    height: 350px;
    margin-top: 0px;
    border: 10px solid white;
}

.grid-item4 {
    grid-column-start: 1;
    grid-column-end: 6;
    grid-row-start: 1;
    grid-row-end: 4;
    background-color: white;
}

.grid-item5 {
   grid-column-start: 6;
   grid-column-end: 7;
   grid-row-start: 1;
   grid-row-end: 4;
   background-color: white;
}

.grid-item6 {
   grid-column-start: 7;
   grid-column-end: 8;
   grid-row-start: 1;
   grid-row-end: 4;
   background-color: white;
}

.grid-item7 {
   grid-column-start: 8;
   grid-column-end: 9;
   grid-row-start: 1;
   grid-row-end: 4;
   background-color: white;
}

// Container 4 //
.grid-container-4 {
   height: 149.5vh;
   border: 10px solid green;
   display: grid;
   grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr;
   grid-template-rows: 1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr;
   grid-gap: 40px;
   margin: 0px;
   padding: 70px;
   background-color: black;
}

.grid-item-A {
   background-color: rgb(115, 105, 105);
   border: 4px solid orange;
   padding: 20px;
}
.grid-item-8 {
   grid-column-start: 1;
   grid-column-end: 4;
   grid-row-start: 1;
   grid-row-end: 4;
   z-index: 1;
}

.grid-item-9 {
   grid-column-start: 2;
   grid-column-end: 5;
   grid-row-start: 2;
   grid-row-end: 5;
}

.grid-item-10 {
   grid-column-start: 6;
   grid-column-end: 10;
   grid-row-start: -10;
   grid-row-end: -8;
}

.grid-item-11 {
   grid-column-start: 1;
   grid-column-end: 5;
   grid-row-start: 5;
   grid-row-end: 7;
}

.grid-item-12 {
   grid-column-start: 5;
   grid-column-end: 10;
   grid-row-start: -7;
   grid-row-end: -4;
}

.grid-item-13 {
   grid-column-start: 1;
   grid-column-end: 6;
   grid-row-start: 8;
   grid-row-end: 10;
}

.grid-item-14 {
   grid-column-start: 7;
   grid-column-end: 10;
   grid-row-start: -1;
   grid-row-end: -3;
}

.grid-item-15 {
   
}
  
// MEDIA QUERIES//
//Mobile Breakpoint
@media (max-width:480px){
   //CODE IN HERE 
   }
   
   //Tablet Breakpoint
   @media (min-width:768px){
      .container-1 > img {
         width: 30em;       
         }
     // container-2 //
      .grid-container-2 > h1 {
         display: grid;
         grid-template-columns: 500px 500px; 
         grid-template-rows: 500px 500px;
         height: 500px;
         width: 30em;
         margin-left: 100px; 
         margin-top: 200px;
         border: 0px solid rgb(9, 9, 9);
         background-color: rgb(10, 8, 8); 
      }
    
      .grid-item {
         background-color: rgb(17, 14, 14);
         border: 0px solid rgb(9, 7, 7);
         padding: 0px;
      }
   
      .grid-item1 {
         grid-column-start: 1;
         grid-column-end: 8;
         grid-row-start: 1;
         grid-row-end: 6;
         margin-right: 300px;
         height: 550px;
         background-color: rgb(9, 4, 4);
     
      }
     
      .grid-item2 {
         grid-column-start: 2;
         grid-column-end: 5;
         grid-row-start: 2;
         grid-row-end: 5;
         margin-right: 600px;
         background-color: rgb(6, 5, 5);
      }

      .grid-item3 {
         grid-column-start: 8;
         grid-column-end: 9;
         grid-row-start: 2;
         grid-row-end: 5;
         margin-left: 0px;
         background-color: white;
      }

      .button {
         background-color: #0c0f0d; /* Black */
         border: none;
         color: white;
         padding: 15px 32px;
         text-align: center;
         text-decoration: none;
         display: inline-block;
         font-size: 22px;
         margin-top: 20px;
         height: 60px;
         width: 245px;
       }

     // container3 //
      .container-3 > h2 {
         width: 30em;
         height: 200px;
      }
      
      .grid-container-3 > h2 {
         display: grid;
         border: 10px white;
         text-align:left;
         margin-left: 200px;
         margin-top: 140px;
         font-family: sans-serif;
         font-size: 100px;
         color: rgb(249, 233, 233);
      }
     
      .grid-container-3 > h2 > p {
         color: rgb(246, 237, 237);
         font-size: 50px;
         font-family: sans-serif;
         margin-top: 70px;
      }
     
     .grid-container-3 > h2 .p {
        color: rgb(250, 242, 242);
        margin: 0px;
        font-size: 25px;
     }
     
      .grid-item4 {
         grid-column-start: 1;
         grid-column-end: 5;
         grid-row-start: 1;
         grid-row-end: 4;
         background-color: white;
     }
     
      .grid-item5 {
         grid-column-start: 5;
         grid-column-end: 8;
         grid-row-start: 1;
         grid-row-end: 4;
         text-align: center;
         background-color: white;
        
   }

      .grid-item6 {
         grid-column-start: 8;
         grid-column-end: 9;
         grid-row-start: 1;
         grid-row-end: 4;
         text-align: center;
         background-color: white;
        
   }

      .grid-item7 {
         grid-column-start: 9;
         grid-column-end: 10;
         grid-row-start: 1;
         grid-row-end: 4;
         text-align: center;
         background-color: white;
   }
   }
   //  container4  //
      
      
   
******Chat Room for Envelope Meeting****

From George Meadors to Everyone 02:22 PM
That is really interesting, because at this point, I still write some of that stuff.  such as bill due dates and the amount and if it's auto pay it let's me know when the money will deducted.
From Neptali Montez to Everyone 02:24 PM
This looks awesome already. I love how straight forward both the app and desktop version are!
From Grace Birnam to Everyone 02:25 PM
^^^
From Daniel Hanna to Everyone 02:25 PM
^^^^^^!!!!!
From Neptali Montez to Everyone 02:26 PM
That would be really cool!
From Jocelyn  Barraza to Everyone 02:26 PM
That’s a great point George we will keep that in mind.
From edwinrodriguez to Everyone 02:28 PM
it is awesome
From Daniel Hanna to Everyone 02:28 PM
Does Contacts pull from the current Contacts app or is it duplicating Contacts?
From Dillon C. to Everyone 02:29 PM
Daniel are you referring to the contact page ?
From Daniel Hanna to Everyone 02:29 PM
Yes
From Dillon C. to Everyone 02:30 PM
that contact page would be for you to contact support just in case there is an issue with an app
From Daniel Hanna to Everyone 02:31 PM
Ohhhh, I thought it was for Contacts such as financial institutions
From Eyob Legese to Everyone 02:31 PM
The level effort and quality work put into this is amazing.
From Neptali Montez to Everyone 02:31 PM
^^^^ I agree!!
From sam to Everyone 02:32 PM
Amazing job!  The wireframe is awesome!
From Daniel Hanna to Everyone 02:32 PM
^^^^^^^ Beautifully done
From Me to Everyone 02:32 PM
^^^^!!!
From Jocelyn  Barraza to Everyone 02:32 PM
Thank you everyone!
From Dillon C. to Everyone 02:33 PM
@Daniel didn't think into that feature but could def be something integrated into the "Household feature"
^But that might be beyond the scope of work as well
From Jocelyn  Barraza to Everyone 02:34 PM
@Klay, great artist <3
From Chai Saetern to Everyone 02:37 PM
love how this is all laid out
From Jocelyn  Barraza to Everyone 02:38 PM
^ right very organized
From Neptali Montez to Everyone 02:38 PM
I agreee ^^
From Chai Saetern to Everyone 02:38 PM
the color palettes remind me of Bob Ross on figma
From Daniel Hanna to Everyone 02:38 PM
The numbers look great and easily legible
From George Meadors to Everyone 02:39 PM
I love Blue. It's an inviting color!  And eye catching!
From Neptali Montez to Everyone 02:39 PM
The logo, the colors, the fonts, BEAUTIFUL!
Definitely super calming and inviting
From Grace Birnam to Everyone 02:39 PM
LOVE
From Darla Brown(She,her) to Everyone 02:40 PM
Great job!
From Me to Everyone 02:40 PM
very asthetic
From Grace Birnam to Everyone 02:40 PM
I really like the runner up logo btw 👀
From Grace Aranico (she/her) to Everyone 02:40 PM
i'm literally vibrating with excitement to get started on this!
From Grace Birnam to Everyone 02:40 PM
reminds me of the Calm app
From Klay Simmons to Everyone 02:41 PM
Thanks so much!
From sam to Everyone 02:41 PM
Awesome design!
From Neptali Montez to Everyone 02:41 PM
Omg yes the Calm app!!
From Grace Birnam to Everyone 02:41 PM
THE PINK ONE
From Emelia Guadarrama to Everyone 02:41 PM
Thanx everyone!
omg that little voice haha
From Jason Smith to Everyone 02:42 PM
I love the choices of colors! Great work!
From Me to Everyone 02:42 PM
Thank You!
From Jocelyn  Barraza to Everyone 02:42 PM
S/O to Juan for including all of us in this project!
From Xavier Mercado to Everyone 02:42 PM
Pretty neat! Will we see these colors applied to the app wireframe?
From Alberto Sandoval to Everyone 02:42 PM
ABSOLUTELY!
From Sandra Juarez to Everyone 02:42 PM
Emelia.. he promised he was going to go take a nap while I worked, lol
From Miles Angels to Everyone 02:42 PM
I absolutely love how organized everything is.
From Emelia Guadarrama to Everyone 02:42 PM
Lol so dang cute haha
From Klay Simmons to Everyone 02:42 PM
Thanks for that Chai! We are all very excited to work with you all
From Chai Saetern to Everyone 02:42 PM
^^^!
From Grace Birnam to Everyone 02:42 PM
that purple envelope omg
From Suman mainali to Everyone 02:43 PM
more respect to Figma
From George Meadors to Everyone 02:43 PM
I second that Chai!
From Jocelyn  Barraza to Everyone 02:43 PM
Lol Sandra I had to kick my brother out my room when I was presenting, he loves asking me questions the minute I get busy haha
From Efrain Gonzalez to Everyone 02:43 PM
We want to see these rabbits multiply like the users money hopefully
From Grace Birnam to Everyone 02:43 PM
I could stare at these colors and graphics all day
From Jacob DiFede to Everyone 02:45 PM
I think a Chinese drop down with other dialects would be cool!
From Neptali Montez to Everyone 02:45 PM
Oh yes !^^
From Lei to Everyone 02:45 PM
sounds good!
From Klay Simmons to Everyone 02:45 PM
Thats a good point thanks for bringing that up Danu
From J to Everyone 02:49 PM
I like that ideas jacob
From edwinrodriguez to Everyone 02:50 PM
how about spending stopper some how
From J to Everyone 02:50 PM
Data is 💯
From Miles Angels to Everyone 02:52 PM
Thank you for choosing a very legible font. I have a hard time reading things off of small screens and certain fonts aren't very legible when scaled down.
From J to Everyone 02:53 PM
This projects is def 👌
Compatibility and user friendly
From Klay Simmons to Everyone 02:53 PM
Daniel thanks for the insight!
From J to Everyone 02:53 PM
Good points George and daniel
From Chai Saetern to Everyone 02:54 PM
Maybe an option to set a recurring bill/subscriptions to know that it will come up the next
month*
From Miles Angels to Everyone 02:56 PM
Did the color scheme undergo testing for color blindness accessibility? I am unsure if my question is relevant but I am curious about it.
From Myeisha ( Mye :) ) to Everyone 02:57 PM
Does the app link to any bank accounts ?
From Emelia Guadarrama to Everyone 02:57 PM
Miles, yeah we've put a few of the colors to the test and will continue that as we progress.
From Dillon C. to Everyone 02:57 PM
No the app doesn't link to any bank accounts, its all manuel
From Daniel Hanna to Everyone 02:58 PM
^^^^^^ Cool
From Miles Angels to Everyone 02:58 PM
Thank you for answering my question Emilia!
*Emelia
From Emelia Guadarrama to Everyone 02:58 PM
yeah of course! We’ve got a lot of great plug-ins in Figma that help us test accessibility
From Myeisha ( Mye :) ) to Everyone 02:59 PM
Awesome thank you Dillon
From Daniel Hanna to Everyone 03:00 PM
By everyone...I need to leave now. Thank you so much for such a great presentation 🤓
From Grace Birnam to Everyone 03:00 PM
my mind works at 59045943x speed
From Emelia Guadarrama to Everyone 03:00 PM
Thank you all so much!
From Darla Brown(She,her) to Everyone 03:00 PM
pay my water bill
From sam to Everyone 03:00 PM
Amazing job!!!!
From Efrain Gonzalez to Everyone 03:00 PM
We're really excited to be working with all of you!
From Klay Simmons to Everyone 03:01 PM
Thank you all!
From George Meadors to Everyone 03:01 PM
Thanks for the invite pals!
From Me to Everyone 03:01 PM
Thanks everyone!!!
From Habteab Firezgi to Everyone 03:01 PM
This app will be great for sure
From Sandra Juarez to Everyone 03:01 PM
Very cool!! I love the collar work and how well you’ve all seemed to work together!!
From Dillon C. to Everyone 03:01 PM
thanks for the feedback everyone, it's all appreciated !
From Jocelyn  Barraza to Everyone 03:01 PM
Thank you everyone!
From Tesfa Worku to Everyone 03:01 PM
Great work pals. The level of talent in this group is amazing. Thank you!
From Jacob DiFede to Everyone 03:01 PM



















