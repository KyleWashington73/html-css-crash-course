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
-Internal CSS is annoying when you want to reapeat the same cahange in multiple places.
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
External CSS= *One file is controlling all of the styles, not the page you are on. If uou delete something from the stylesheet, or change something, it is changing for all the pages.*
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















*You can also control the border of the different sides independently:
                .example  {
                  border-left: 2px solid pink;
                  border-right: 5px dotted red;
                  border-bottom: 10px double green;
                  border-top: 1px dashed purple;
                  }














