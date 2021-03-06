# Learn to Code - Intro to CSS

Brought to you by Galvanize. Learn more about the way we teach code at [galvanize.com](galvanize.com).

## Overview

The goal of this brief course is to provide you with a fun introduction to the world of web development, focusing on CSS. We will explore a variety of ways to build CSS features, and if we have time, we'll explore some CSS3 as well.

#### Here's what we'll be doing:

* Setting up our computers for web development
* Setting up your HTML with CSS
* Basic CSS syntax and features
* Advanced CSS features
* Playing around in the sandbox

**This course presumes some knowledge of HTML.** If you need to review, check out [our course](https://github.com/GalvanizeOpenSource/learn-to-code-intro-html/) at the link below.

_Learn To Code HTML_: [https://github.com/GalvanizeOpenSource/learn-to-code-intro-html/](https://github.com/GalvanizeOpenSource/learn-to-code-intro-html/)

#### Before you begin, a quick gut check:

* This course is for absolute beginners
* Feel free to move ahead
* Help others when you can
* Be patient and nice
* You will get through it!

#### What web coding is (really)?

Recipes to give to your computer to “cook” up some awesome things for you online

## Setting up your computer

(Brace yourself...)

#### Please set up the following:

* A web browser to see what we're working on as others see it (Recommend Google Chrome: chrome.google.com)
* A text editor to modify your files (Recommend the Atom text editor: [Atom.io](Atom.io))
* Download the tutorial files on this page within the zip file

####  Download the file for this class:

1. Go to https://github.com/GalvanizeOpenSource/Learn-To-Code-Intro-CSS
2. Click on the button on the right-hand side that says "Download ZIP"
3. Go to your downloads folder and double click on the .zip file to unzip it
4. From Atom: File > open, select the folder and then click "Open"
5. From Atom: If the file tree does not appear on the left hand View > Toggle Tree View -- this will show you the entire folder within Atom
6. Open up the file in your browser -- 
  a. index.html
  b. style.css

#### Alternative: Use CodePen to code for this course

1. Go to this link: [https://codepen.io/leepngo/pen/KgrLNw](https://codepen.io/leepngo/pen/KgrLNw).
2. You will be taken to a page where you can simulate the coding experience.
3. Focus on the windows called "HTML" and "CSS". We'll work mostly in that one. Feel free to minimize the "JS" window.

**Patience!** Setting up your computer takes time and can be tricky, especially across platforms.

Once you're ready, you can move onto the next lesson.

## Overview of CSS

#### What Does CSS Stand for?

* _Cascading_ - prioritizing certain values over others
* _Style_ - focusing on layout, colors, fonts, etc.
* _Sheet_ - another name for the file we use here
The internet used to be ugly. Enter CSS - a consolidated way to make it prettier.

#### Three primary objects:

* _Elements_: e.g. h1, div, body, a - default HTML (already reviewed)
* _Classes_: everything that starts with a “.”
* _IDs_: everything that starts with a “#”

#### Elements

We're going to start you off with a prepared HTML page that looks like this.

```html
<html>
  <head>
    <title>
      Hello! Learn to Code CSS with us!
    </title>
  </head>
  <body>
    <header>This is a header. Make it look better.</header>
    <h1>This is a vertical navigation bar.</h1>
    <nav>
      <ul>
        <li>Header</li>
        <li>Text #1</li> 
        <li>Text #2</li> 
        <li>Footer</li> 
      </ul>  
    </nav>
    <div>
      This is a wall of text. What can you do to make it more visually appealing in this webpage? Right now, it sure could use a little style.
    </div>  
    <h1>This is a horizontal navigation bar.</h1>
    <nav>
      <a>Header</a> | <a>Text #1</a> | <a>Text #2</a> | <a>Footer</a>
    </nav> 
    <div>
      This is a wall of text. Can you make it look like the last wall of text without having to write too much code?
    </div>
    <div>Can you change some of the words in this text to the same color? What if you wanted to change them to a different color? How would you do that? 
    <footer>This is a footer. Make it look better.</footer>
  </body>  
</html>
```

If you don't remember HTML, now is a good time to review the [HTML course](https://github.com/GalvanizeOpenSource/learn-to-code-intro-html/).

**ONE CHANGE:** For those of you working in Atom, you have to "connect" your CSS file to your HTML file.

You can do so with the following code in the header:

```html
  <head>
    <title>
      Hello! Learn to Code CSS with us!
    </title>
    
    <link href="style.css" rel="stylesheet type="text/css" /> <!-- Add this line to your code -->
    
  </head>
```  

We'll be adding CSS classes and IDs into this HTML, but first, an overview of the syntax.

## Syntax of CSS:

```css
h1 {  // this is either an element, class, or ID
    font-size: 24px; // syntax is name: value;
    font-weight: bold;
    color: #000000; // hexadecimal, RGB, etc.
}
```
Space doesn’t matter, but “onion” rules apply

#### What are Classes?

Classes are attributes something to multiple elements on a page noted with a “.” symbol in CSS.

Below is an example.

HTML:
```html
 
<a class=”ninja”>Lee Ngo</a>
```

CSS:
```css
.ninja { 
    color: black; margin: 10px; 
}
```

Classes are used to change or affect multiple items in an HTML document at once

e.g. everything with class=”ninja” should have the same attributes

## LET'S CODE!

**Remember:**

* Coding can be hard - be patient!
* Work in pairs! Even the pros do it
* Ask for help - we’re in a school!

#### Let's create our first class

Improve the blocks of text with some style. First, let's build a CSS class that pads it a little and changes the front to something... nicer.:

```css
.text-block {
    padding: 20px;
    font-family: Trebuchet MS;
}
```

We're not done yet! Add the class `text-block` into the first HTML element. No need for the "." in HTML.

```html
    <div class="text-block">
      This is a wall of text. What can you do to make it more visually appealing in this webpage? Right now, it sure could use a little style.
    </div> 
```

_Did something change?_ What happens if you add the class `text-block` to the other HTML `<div>` element with text?

**Keep going!** Let's do some more challenges.

#### Let's add some style to the header

First, let's create a new class called `.header` in the `style.css` file and give it the following attributes:

_style.css_
```css
.header {
    height:50px;
    background:#D9D9D9;
    border:1px solid #CCC;
    width:960px;
    margin:0px auto; 
}
```
There's a lot going on here, but basically, we're adding a lot of different styles to a single class.

Now, let's add that class into our HTML element. 

```html
    <header class="header">This is a header. Make it look better.</header>
```

Refresh your browser - _do you see a difference?_

_Feeling ambitious?_ Try the next exercise:

#### Improve the <nav> bar

There's a navigation menu in there, but it doesn't look great. Add the following code into your CSS page.

```css
ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
    width: 200px;
    background-color: #f1f1f1;
}

li a {
    display: block;
    color: #000;
    padding: 8px 16px;
    text-decoration: none;
}

/* Change the link color on hover */
li a:hover {
    background-color: #555;
    color: white;
}
```

Navigations are structured as lists in HTML, so we're telling CSS to perform in certain ways. 

Add a few links into your `<nav>` items and see if the effect takes place.

#### What are IDs?

IDs are attributes that are used only on one element ONLY and noted with a “#” symbol in CSS e.g.

HTML:
```html
<a id=”leesName”>Lee Ngo</a>
```

CSS: 
```css
#leesName { 
    color: white; 
}
```

IDs are used to direct functions to unique elements in the HTML so that there’s no confusion

e.g clicking to a specific part of page

In tandem, you can do a lot with HTML & CSS! Let's give it a shot!

## LET'S CODE

Let's use the second `<nav>` bar to navigate to specific parts of the page. Let's create some anchor tags into the nav bar to make the items "clickable."

```html
    <nav>
    <!-- add code below -->
      <a href="#header">Header</a> | <a href="#text-1">Text #1</a> | <a href="#text-2">Text #2</a> | <a href="#footer">Footer</a> 
    <!-- add code above -->
    </nav> 
```
Now add corresponding id designations to the various HTML tags. Don't use the "#" symbol.

```html
<html>
  <head>
    <title>
      Hello! Learn to Code CSS with us!
    </title>
  </head>
  <body>
  <!-- add code below -->
    <header id="header">This is a header. Make it look better.</header>
  <!-- add code above -->  
    <h1>This is a vertical navigation bar.</h1>
    <nav>
      <ul>
        <li>Header</li>
        <li>Text #1</li> 
        <li>Text #2</li> 
        <li>Footer</li> 
      </ul>  
    </nav>
    <!-- add code below -->
    <div id="text-1">
    <!-- add code above -->  
      This is a wall of text. What can you do to make it more visually appealing in this webpage? Right now, it sure could use a little style.
    </div>  
    <h1>This is a horizontal navigation bar.</h1>
    <nav>
      <a href="#header">Header</a> | <a href="#text-1">Text #1</a> | <a href="#text-2">Text #2</a> | <a href="#footer">Footer</a> 
    </nav> 
    <!-- add code below -->
    <div id="text-2">
    <!-- add code above -->  
      This is a wall of text. Can you make it look like the last wall of text without having to write too much code?
    </div>
    <div>Can you change some of the words in this text to the same color? What if you wanted to change them to a different color? How would you do that? 
    <!-- add code below -->
    <footer id="footer">This is a footer. Make it look better.</footer>
    <!-- add code above -->  
  </body>  
</html>
```
Great! Now save your work and click on your new links. _What happens?_

**Advice** Try not to use IDs as selectors. They could lead to problems in your code moving forward.

## PLAY IN THE SANDBOX

You have the basics down. Try doing more - look up online for those options:

1. Change the background of the entire webpage
2. Add some buttons - they're nicer-looking than links
3. Try importing [Bootstrap](http://getbootstrap.com/) and playing around with it
4. Can you do animations in HTML/CSS alone...?

- Show what you did with the others! 

# YOU DID IT! YOU'RE NOW A CODER!

Welcome to the cool kids club.

#### Want to code more? Check out Galvanize's Full Stack Immersive Program!

- 24 Week Full-Time Program
- High Job Placement Rate within six months
- Average starting salary: $77,000 per annum
- Scholarships available for those who qualify
- Learn more at [http://galvanize.com/courses/web-development/](http://galvanize.com/courses/web-development/)

#### Looking for something more flexible? Check out our  Workshops!

- Zero to Web Designer
- Foundations of JavaScript
- Web Development Immersive Prep
- Learn more at http://www.galvanize.com/workshops/

#### About the Authors

[Lee Ngo](http://linkedin.com/in/leengo) is an evangelist for Galvanize based in Seattle. Previously he worked for UP Global (now Techstars) and founded his own ed-tech company in Pittsburgh, PA. Lee believes in learning by doing, engaging and sharing, and he teaches code through a combination of visual communication, teamwork, and project-oriented learning.

You can email him at [lee.ngo@galvanize.com](mailto:lee.ngo@galvanize.com) for any further questions. 
