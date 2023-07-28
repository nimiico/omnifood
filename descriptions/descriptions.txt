resources page: jonas.io

# HTML

example: paragraph element -> <p>(opening tag) content(also images have no content) </p>(closing tag)

## extensions: 
- image prewiew
- auto rename tag
- live server
- color highlight

##HTML Entities

## settings
- auto close tag

## Start

1. <!DOCTYPE html> # declare doc type to tell the browser that this doc use hTML.
2. <html></html> # html element
3. <head> </head> # head element inside html element (include title, additional info about page, link to css files, ...)
* <title></title> # subset of head (inside of head)
4. <body></body> #  body element next and out of head but inside of html element
5. <h1></h1> # head of text that has h1 to h6 and go to smaller size of font (every page should be have h1)
6. <p></p> # paragraph
7. <!-- --> # comment
8. 
  - <strong></strong> # bold a part of text
  - <b></b> # bold a part of text
  - <i></i> # italic a part of text
  - <em></em> # italic a part of text
  - <figure></figure> # standard form for cards or galleries because has <figcaption></figcaption> inside of it
  - <blockqoute></blockqoute>
  - <table></table> # table
  - <tr></tr> # table row
  - <td></td> # table data
  - <thead></thead> # table head. the first row
  - <tbody></tbody> # table body
  - <th></th> # head of each column and row
  - <main></main> # main content of the page, out side of the main be somthing like headers that same in different page of our website or footer
  - <form></form> # a box that input element, put into it.
9.
  - <ol></ol> # order list
  - <li></li> # for each item of list and it must be in ol
10.
  - <ul></ul> # unorder list
  - <li></li> # for each item of list and it must be in ul
  
### attributes
11. 
  - <img src="directory of image" alt="description of image" height="" weight="" />
  - <html lang="en"></html> # html element and set language
  - <meta charset="UTF-8" # set character
  
12. href is attribute that create link
  - <a href="url">title of link</a> # open website that is outside of our website in this tab 
  - <a href="url" target="_blank">title of link</a> # open website that is outside of our website in new tab
  - <a href="name of html that you create for example: blog.html">title of link</a> # open page that is inside of our website in this tab 
  - <a href="#">title of link</a> # open nothing and just go to above the webpage

13.
  - <nav></nav> # group navigation links in a container
  - <header></header> # group header text like h1 or somthing like this that we want separate them from other contents
  - <article></article> # group other content except header
    - <header></header> # group header content of article

14. <aside></aside> # group that is the closure of main content
15. <footer></footer> # craete a footer
16. <div></div> # for group contents when we use this element the group has no semantic meaning for us and just we want group them
17. <input type=""> # input element

# CSS

## Inline 
<h1 style="color : blue"></h1> declare style in html's elements

## Internal
<style> h1 {color: blue}></style> # declare style element in head.

## External 
h1 {color: blue} # create css file write code like this.
<link href="directory of css file" rel="description" /> # link html file to css file

## Selector Examples
 
example1:
h1 {
  color: #1098ad; # font color
  font-size: 26px; # font size
  font-family: sans-serif; # kind of font
  text-transform: uppercase; # characters form
  font-style: italic; # style
  text-align: center; # alignment
  background-color: #f7f7f7; #background color
}

example2:
h1,h2,h3,h4,p,li {font-family: sans-serif; } # we can list selector to attribute the same features to them

#id {font-family: sans-serif;} # specify selector by id (id is unic) we dont use id mainly.
.class {font-family: sans-serif;} # specify selector by class
/* */ # comment

example3:
.related-list {list-style: none;} # points remove

## colors
rgb : #ff ff ff (hexadecimal)

example4:
.related-aside {
  background-color: #f7f7f7; # background color
  border-top: 5px solid #1098ad; # border top size, form, color
  border-bottom: 5px solid #1098ad; # border bottom  size, form, color
}

example5:
li:first-child {
  font-weight: bold; # convert all first item of every li elements to bold.
}

example6:
li:nth-child(2) {
  color: #1098ad; # colored second item of every li elements.
}

example7:
article p:last-child {
  color: #1098ad;       #colored the last child of article if it was p, but if p was not the last on this code is incurrect.
}

## Link Styles
a:link {
  color: #1098ad;        # link style
  text-decoration: none; # underline of links
}

a:visited {
  color: #1098ad;  # link that visited style
}

a:hover {
  color: orangered;
  font-weight: bold;			# when you move mouse on link style
  text-decoration: underline  orangered;
}

a:active {
  background-color: black;	# when you click on link style
  font-style: italic;
}

## chrome dev tools
right click >> inspect >> elements 

- on right side you can see style of each part you click on it

* {
  color:red;  # all of elements get red color
}
	

## Resolve conflicting delaration
priority (high to low): #id -> .class -> element selector(p, li, div, ...) -> universal selector(*) and in same priority the last one is higher priority yhan other
priority (high to low): psudo class -> element selector

## Inheritance 
some properties (like text)  get inherited from parents to child but can easily overwrite same properties that there is in child.

## The CSS box model
1.content # text, image, table, ...
2.border # line around box
3.padding # space inside
4.margin # space outside

- if you margin-bottem for top element, and margin top for bottem element, the bigger one applied.
example1:
.main-header {
  padding-left: 40px;
  padding: 20px 40px; # bottem-top  left-right
  margin-bottom: 60px;
  width: 500px; # width of element box
}

example2:
.post-img {
  width: 100%; # 100% of container(parent) of the current element width
  height: auto;
}

example3:
.container {	# all of elements are in container
  width: 700px; # the children not be wider than parent.
  margin-left: auto; # means margin of left equals right and depends on page size (as a result container been in center)
  margin-right: auto;
}

## different boxes or elements
1. inline boxes # spacing content's size (strong, a, ...) -> margin and padding applies in horizontally not top or bottom
nav a:link {
  display: block; # convert to block level
}

2. block-level boxes # spacing all of parent's element width
nav a:link {
  display: inline; # convert to inline
}

3.inline-block box 
- looks like inline (spacing content's size), behave like block level (margin and padding applies all of side)
nav a:link {
  display: inline-block; # convert to inline-block
}

## Positioning
1.normal flow
2.absolute positioning # fixed

example1:
position: relative; # in this example is parent
button {
  position: absolute;
  bottom: 50px;		# child # this absolutely fixed (with 50px from right and 50px from bottom of parent that set to relative.
  right: 50px;
}

## Psudo elements

example1:
h1::first-letter {
  font-style: normal;
}

example2:
h3 + p::first-line {  #the p elements that are exactly next of h3s first line (adjancy elements)
  color: red;
}

### Create psudo element in css # no exist this element in html
example:
h2 {
  position: relative; # for position the child, parent must be relative
}

h2::after {			#create element after h2
  content: "Top";
  color: #444;
  background-color: #ffe70e;
  font-size: 16px;
  display: inline-block;
  padding: 5px 10px;
  position: absolute;
  top: -10px;
  right: -25px;
}

# CSS LAYOUTS

- layout is a way that include text, image, ... that arranged on webpage
- page layout is include components layouts that are in webpage
- component layouts is part of a page loyout that include some contents

## Float Layouts

example1:
.auther-image {
  float: left ;			# float-left is connecting to leftmost side since get to an element and likes taht remove from normal flow
  margin-bottom: 20px;
}
.auther {
  margin-left: 20px;
  margin-top: 10px;
  float: left;			# float-left is connecting to leftmost side since get to an element (auther-image) 
}

### fix colapse (clearfix hack) to resolve the colapsing in float layouts. 
-first you craete another class in html for your element(clearfix in example) then you create psudo element(after) give it content and convert it to block to fix colapse.
.clearfix::after {
  clear: both;
  content: '';
  display: block;
}


### Box sizing
box-sizing: border-box;  # change size of things that are in border to fix the best size of the single elements, so it's better at first we add this code in to a * selector. 

## FlexBox      # add image of properties to github

- it is a flex container with some flex child (flex items) that they were placed side by side
- has cross axis andmain axis

some of properties:
*notice: their properties are apply to all of items and this code write in element that all of items are subset of it.
  display: flex;
  flex-direction: column; # all things and properties rotates 90 degrees. for ecxample align-items, align items horizonyally, no longer vertically and so on...
  align-self: stretch # strech to the highest item
  order: number # default all of items order is 0 and we can change this order
  flex-basis: 200px; # all of items that are smaller than 200px get to 200 and other ones that their content bigger than 200, their width fixed to their content width.
  flex-shrink: 0; # 0, 1, 2, ...  (numbers is like order and when increase that item sise also increase)-> active or deactive # if be 1 the items generally can not bigger than container even flex basis is muuch and limit  size of items and default is 1
  flex-grow: 1; # 0, 1, 2, ... (numbers is like order and when increase that item sise also increase)-> if its 1 the items extend to fill remaining space of container
  flex: 0 0 200px # flex-grow flex-shrink flex-basis
  
  ## CSS Grid
- we have a grid container that includes grid items
- divide in column and row child element
- grid css has gridlines that they divide container to different parts, these parts called grid cells that grid items get into these cells also zthese cells might be not fill by items and be empty
	if we have for example 2 rows, grid line is 3 and so on...

### Auto grid cells sizing
display: grid;
grid-template-columns: 250px 150px; # generate 2 columns with 250px and 150 px width
grid-template-columns: 1fr 1fr; # when you set the column width 1fr fill the container and it is flexible so if you set 1fr to 2 column boyh of them have same size and flexible (2fr is 2 times bigger than 1fr)
grid-template-columns: 1fr 1fr == grid-template-columns: repeat(2, 1fr);
grid-template-columns: auto; # take space that it needs
column-gap: 30px; # column gap

also row has above instruction
grid-template-rows: 300px 200px; # for rows 
row-gap: 60px; # row gap

### Manualy grid cells sizing

indexing guidlines: 1, 2, 3, 4 or -4, -3, -2, -1
grid-column: 1 / 3; # from 1 to 3 column guideline
grid-column: 1 / span 3; # start from 1 and span across three cells
grid-row: 2 / 3; # from 2 to 3 row guideline

### aligning tracks inside the containers
justify-content: center; # aligning horizontally
align-content: center; # aligning vertically

aligning items inside the cells:
align-items: center; # aligning vertically
justify-items: center; # aligning horizontally

align-self: center; # aligning vertically for one item
justify-self: center; # aligning horizontally for one item

# WEB DESIGN

## Design Ingredient

### Typography # making text beautiful

Tools -> Google Fonts, Font Quirrel

- serif # classic and treditional # merriweather, aleo, playfair display, cormorant, cardo, lora
- sans-serif # clean and simple / modern # inter, open sans, roboto, montserrat, work sans, lato

#### Rules
1. use good and popular types
2. use limit 2 types
3. choose right types according the web personalities
4. use font size beetwen 16px to 32px for normal text
5. for long text use 20px or bigger
6. headlines more than 50px and bold 600+
7. for any text use font weight 400+
8.use less than 75 characters per line
9.line height for normal size must be between 1.5 to 2 and forbig text below 1.5
10. decrease letter spacing if it's unnatural
11. for short titles you can make them small and bold and increase letter spacing 
12. don't justify the text
13.don't center long text block
14. start with smaller size in header before main header.

## project
1. for add font type from google font, just copy link of current fnt styles and then paste it into the html file then add the name of font-family that you choose to css file like: font-family: 'Inter'

## Color

1. color personality
  red -> attention, power
  orange -> happines
  yellow -> brightness and intelligence
  green -> nature, grow, health
  blue -> peace, trustworthiness
  purple -> wisdom, magic
  pink -> romance, care
  brown -> nature, comfort
  black -> minimalism
2. color tone  -> open color
3. main color, grey color( dark form of main color) and lighter and darker version of this colors -> palleton.com, coolor, maketintsandshades (for tints and shades
4. draw attention for important elements like logo, button, ...
5. highlights, underlines, color text
6. use color stratigically same with images
7. in dark background use the lighter version of background color for text
8. text shoud not completly black
9.contrast ratio at least 4:5:1 for normal text, 3:1 for large text

## Images _> unsplash, pexels, drawkit, undraw, uifaces
1. storytelling images, patterns, product photos
2. original images, high quality stock photos
3. use real people photo
4. combining photos
5. darker or brih=ghten image for readble text
6.put text into netralimage area
7. make image dimensions 2x as big as their displayed size for high res displays
8. compress for lower file size and better performance # tools -> squoosh
9. same hieght in side by side

## Icons -> phosphors icons, heroicons, ionicons, icons8
- copy svg and paste it into html file and create class for that for set features in css file
1. use one icon packs
2. use icon svg format and icon font
3. we use icons for provide visual assistance to text
4. use icons in feature blocks
5. in actions (items, buttom, ..) it's better to we use both icon with text not just icons 
6. never use some feature just icon and some features by text side by side
7. use icons as bullet points
8. to keep icons neutral , use same color as text. to draw more attention, use different colorheroicons 
9. don't use icon larger than what way were designed for

## Shadows

1. more serius and elegant use less shadows and more funny more shadows
2. don't use shadows for all elements, for example for seperate top and bottom elements or for stand out of the rest
3. go light shadows, and don't make too dark
4. smalls shadows for smaller elements that we want stand out of the rest (to dra attention
5. medium size shado for large areas that should atand out a bit more 
6. large shadows for element should really float above the interface like pop-up windows
7. changing shadows for example when hover with the mouse has large shadows and when we click like that it get close to interface and shadows get smaller and some effects like this
8. colored shadows (glows)

box-shadow: 20px 20px 20px 10 red; # 1.(horizontal) 2.(vertical) 3.(blur) 4.scale-shadow 5.color\
text-shadow: 0 5px 3px rgba(0, 0, 0, 0.07); # 1.(horizontal) 2.(vertical) 3.(blur) 4.color (usually use for texts that are on top of the images)

## Border Redius
1. less redius so more elegant and serious

border-radius: 100px;
border-bottem-left-radius: 20px;

## White Space
1. between sections
2. between deifferent groups of elements
3. between smaller elements
4. inside groups of elements
5. start with a lot whitspace and then remove white space from there

## Visual Hierarchy
1. position important elements closer to the top of the page
2. use images mindfully, because thae get alot attention
3. use different font size color font weight and space to convey importance because these items get attention
4. emphasize an important components by using background color, shadow, border, ...
5. emphasize component A over B, you can de-emphasizing B

## User Experience (UX)
look likes and feels like -> UI
how it works -> UX

1. doesn't use complicated layouts
2. make your call action more prominent element
3. use blue text or underlined text only for links
4. animations must have apurpose and fast. between 200 to 500 ms
5. easier to scan
6. good feedback for all actions: errors, form success, ...
7. use descriptive, keyword-focused headline 
8. break upwith subheadings, images, blletpoints, ...

## web design sites -> land-book.com, onepagelove.com, awwwards.com

## Components and Layouts Patterns
some example in common file.

1.
- transform: scale(1.5); # scale element size
- transform: translate(-50%, -50%); # move as much as 50% width and height of element also you can put 'px'
- padding: 32px 48px 32px 86px; # top right bottom left

2.
- border-collapse: collapse; # colapse border line that are side by side
- tbody tr:nth-child(odd) {
	background-color: #f8f9fa; # coloring odd ones

3.
- .page-link.page-link--current {     # when it does not have space between two classes it means selector has two classes and it effect on priority
        background-color: #087f5b;  
        color: #fff;                  
      }
      
4.
- height: 100vh; # 100% of view port. 100% of the screen height

- position: absolute;
- left: 50%;                          # positioned in center of parents reletively so the parent must position: reletive. and then it get in to center of parent in every size
- top: 50%;
- transform: translate(-50%, -50%);

- background-image: url(img/hero.jpg); # set image for background
- background-size: cover; # fixed iamge in it aprent
- background-image: linear-gradient(rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.6)), url(img/hero.jpg); # mixed to image that first is on top of the second
- background-image: linear-gradient(rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.6)) # gradiant from first color to second color

5.
- margin-left: auto; # margin from flexible by size of the window
- overflow: scroll; # How elements taht don't fit into container apear

1.Fluid Layouts
- use %, vh, vw instead of px
- use max-width instead of width

2.Responsive Units
- use rem unit instead ofpx
- setting 1rem to 10px

3.Flexible Images
- use % for image dimensions, max-width

4. Media Queries
- to change css style on certain viewport width (called breakpoints)

## WEB DEVELOPING PROCESS
1. Define the project
- who the website is for
- what the website is for
- target audiencce

2. Plan the projecy
- website content
- map of site
- define webite personallity

3.sketch layout and components ideas
- layout patterns
- experiment with different components and layouts

4. Design and build website
- design and build website with html and css
- create and design based on selected website personality


5.Test and optimize
- works well in all majors(chrome, ...)
- test the website on actual monile devices not just in DevTools
- Optimize all images
- color contrast issues
- run the lighthouse performance test in chrome DevTools and try to fix reported issues
- search engine optiization

6. launch the masterpiece
- upload your website file on hosting platform like Netlify
- choose and buy graet domain name memorable and easy to write
max-width: 1000px;
7. maintain and keep update
- update over time
- install analytic software (e.g. google google analytics and fathom)
- inform future changes
- blog

## Responsive and Media Queries

- <meta name="viewport" content="width=device-width, initial-scale=1.0" /> # alwaysinclude this line of code
- 1rem = 1em # use em instead rem in media queries
- @media (max-width: 84em) {
  .hero {			# put new properties in media query for different screen sizes range 
    max-width: 120rem;
  }
-  @media(max-width: 75em) {
    html {
      /* 9 / 16 */
      font-size: 56.25%;
    }
 }
 
- how to change visblity of element
  .main-nav {
    /*Hide Navigation */

    /* 1. Hode it visually */
    opacity: 0;

    /* make in unaccessible to mouse and keyboard */ 
    pointer-events: none;

    /* Hide it from screen readers */
    visibility: hidden;
  }

  .nav-open .main-nav {
    opacity: 1;
    pointer-events: auto;
    visibility: visible;
  }

  .nav-open .icon-mobile-nav[name="close-outline"] {
    display: block;
  }

  .nav-open .icon-mobile-nav[name="menu-outline"] {
    display: none;
  }

## Project example

### BORDER
- box-shadow: inset 0 0 0 3px #fff; # trick to add border inside
- border-bottom: 1px solid transparent; # border bottem is more beautiful yhan text decoration and transparent means colored to the parent color

### ANIMATION
- transform functions
- transition: all 0.3s; # animation that all means background-color and color you can also choose one of them and 0.3s means period of time
- transform: translate(2rem, 2rem); # when put this in hover it's move in the direction X, Y when you hover mouse on it and for better animation change box shadows 
- transform: scale(1.1); # 1.1 times bigger
- overflow: hidden; # doesn't permission to element get bigger than default size (use in parents usually) for example when we use 'transform: scale()' the element overflow the size of it and we can hidden it.
- overflow-x: hidden; # hidden overflows that are in x axis
- transform: translateX(100%);
- transform: translateX(0); # transform is smooth in animations so use it when you want shift element 
- - transition: all 0.3s east-in; # at first move slow and then go fast (east-in-out # fast first and end and slow middle)

### RESPONSIVE DESIGN
- max-width: 1000px; # when the web page be more than 1000 the element size will be 1000px, but when the window get less than 1000px the element adapt with that.
- set rem -> at first we must set the font-size in html selector to 62.5% (because of deafult font-size in browser is 16px = 1 and we convert it to 10px for easy calculate. also if the deafult vlue(16px)  was another value our page become responsive (because of the percentage) when we set it to 62.5%, rem become 10px. then we use rem instead of px.

### GRID
- grid-template-columns: repeat(2, 1fr); # grid-template-columns: 1fr 1fr

### Width
- hero section is better to wider
- uppercase and some space between
- .container {
  max-width: 120rem;
  padding: 0 3.2rem;  # flexible container
  margin: 0 auto;
}

- padding-bottom: 60%; # 60% of parrent's width

### POSITION
- z-index: -1; put more behind
z-index: -2; # more behind

### IMAGE
- filter: functions; # filtering and editing
- opacity: 50%; # visiblity view
- background-image: linear-gradient(to right bottom, red, #e67e22); # change color from red to orange, start at the left top
- background-position: center; # shoo center of your image if the parent size is smaller than image size
- <div
      class="cta-img-box r"
      role="img"                        # define div as image element without using img element
      aria-label="Woman enjoying food"
></div>

### PSUDO CLASS
- .grid:not(:last-child) {  
  margin-bottom: 9.6rem;   # not psudo class
}

### HTML CODE
- <main></main> # main content of the page, out side of the main be somthing like headers that same in different page of our website or footer
- <form></form> # a box that input element, put into it.
- <input type=""> # input element
- <form class="cta-form" action="#"></form> # action is for address of place that we want send data
- <label for="full-name">Full Name</label>   # label of bottom input and for is for connect label to input
    <input id="full-name" type="text" placeholder="Nima Eslami"> # tint text in input
- <label for="select-where">Where did you hear frgit config --global --add safe.directory /mnt/D4F26588F2657022/projects/html-css-projects/omnifoodom us?</label>
   <select id="select-where"> #selection element
     <option value="">Please choose one option:</option> # option of selection, value is value that it return 
     <option value="friends">Friends and family</option>
   </select>
- <input type="" required> # you must fill input and if you do not that it shows you some error
- it is better to put the input, select, ... in div element to group them
- <a href="tel:415-201-6370">415-201-6370</a> # go to call app
- <a href="mailto:hello@omnifood.com">hello@omnifood.com</a> # for mail go to mail app
- <br /> # get element to next line in html coding

### FORMS
- font-family: inherit; # inherit font family of parents because inputs or buttons font family don't get font family that we set in body automatically 
- color: inherit; # also for color
- outline: none;
  box-shadow: 0 0 0 0.8rem rgba(253, 242, 233, 0.5)   #set outline for knowing that where are you (it can be use every where)
  
### Navigation
- first take id to element that you want navigate to it by clicking then write your id in href of that anchor
- scroll-behavier: smooth # scrolling smooth for vavigations. put it into html selector. but doesnt work on safari

### OPTIMIZING
- caniuse # a website that you will can check the properties that are they support by wich web browser
- lighthouse # a propery in inspect for check performance
- squoosh # for decrease image size,convert imagie from png to webp
- <meta
      name="description"
      content="Omnifood is an AI-powered food subscription that wiil make you eat healthy again, 365 day per year. It's teilored  to your personal tasted and nutritional needs." # description of site
  />

- <link rel="icon" href="content/img/favicon.png"/> # icon of site
- <link rel="apple-touch-icon" href="content/img/apple-touch-icon.png" # apple icon homescreen
- <link rel="manifest" href="manifest.webmanifest" /> # android
- {
  "icons": [
    { "src": "content/img/favicon-192.png",
     "type": "image/png",
    "sizes": "192x192 "},				# manifest content
    { "src": "content/img/favicon-512.png",
     "type": "image/png",
    "sizes": "512x512 "}
  ]
}

-<picture>
              <source srcset="content/img/hero.webp" type="image/webp" />
              <source srcset="content/img/hero-min.png" type="image/png" />
              <img
                src="content/img/hero-min.png"
                alt="woman enjoying food,					# because of some web browser doesn't support webp. this form code for images choose the most appropriate form og image.
                meals in storage container"
                class="hero-image"
              />
</picture>
   
### LAUNCHING
- netlify
  





