## Stylesheets  

- **Use Normalize.css**  
In their own words: "It makes browsers render all elements more consistently and in line with modern standards."  
It is better to use [Normalize.css](http://necolas.github.io/normalize.css/)   than a standard reset.css, because it keeps useful defaults rather than unstyling all elements.  

- **Never use inline styles**  
Keep the styles out of the HTML. Think separation of concerns. It makes mainteanance much easier.  

- **Target IE with specific stylesheets**  
```
<!--[if lt IE 7] >
    <link rel="stylesheet" href="ie.css">
<![endif]-->
```  

- **Compress your CSS when you're done**  
A compressed file is smaller, thus faster to load.  
You can use [CSS Optimiser](http://www.cssoptimiser.com/), [CSS compressor](http://www.csscompressor.com/), [Clean CSS](http://www.cleancss.com/)  

***

## General

- **Use CSS3 techniques**  
A lot of CSS3 properties can be used right now. You can freely use border-radius, box-shadow, text-shadow, rgba, opacity, multiple backgrounds, resize, transitions, etc.  
Check on [CanIUse](http://caniuse.com/) or [HTML5Please](http://html5please.com/#css) for up-to-date compatibility tables.

- **Style all elements !**  
You might not need a blockquote at first launch, but that doesn't mean it won't ever be needed. Plan for every possible case !



- **Do not use '!important', ever**

- **Use 3-digit hexcodes when possible**  
Bad
```
p {
    color: #333333;
}
```  
Good
```
p {
    color: #333;
}
```

- **Use shorthands**  
Bad
```
div {
    margin-left: 5px;  
    margin-right: 7px;  
    margin-top: 8px;
}
```  
Good
```
div {
    margin: 8px 7px 0px 5px;
}
```

- **Understand the difference between block and inline elements**  
And never put a block element inside an inline element.  

- **Use absolute positioning sparingly**

- **Use multiple stylesheets on development**  
Just make sure you combine them into one file in production to minimize HTTP requests.

- **Organize your stylesheets**

- **Add meta to your stylesheets**  
Like who is the author, how to contact him, the date of the last update. A reference to your repetitively used colors. 

- **Learn about CSS preprocessors**  

- **Try Object Oriented CSS**

***

## Structure

- **Use comment blocks to separate sections of your page**  

```
/*=============================================================
* Header
==============================================================*/
header {
    ...
}
...

/*=============================================================
* Content
==============================================================*/
.content {
    ... 
}
...
```

- **Try alphabetizing your properties**

***

## Selectors

- **Use hyphens instead of underscores**

- **Keep your selectors short**  
Bad 
```
body #container .someclass ul li {...}  
```  
Good 
```
.someclass li {...}  
```

- **Don't over-qualify your selectors**  

- **Avoid IDs, use classes instead**

- **Your CSS classees should describe the content, not the look**

- **Place one selector per line when using multiple selectors**  
Bad 
```
.menu-primary, .menu-secondary, #header .menu {
	background-color: #fff;
}
```  
Good
```
.menu-primary,
.menu-secondary,
#header .menu {
	background-color: #fff;
}
```

***

## Utilities  

- **Use generic classes**  
There are some styles that you apply over and over. Create generic classes for those styles, instead of applying these styles to each element individually.  
```
.left {
	float: left;
}
```
  
- **Use the Micro Clearfix**  
This method has been used for a while to clear floats:  
<pre><code>
&lt;div class="clear"&gt;&lt;/div&gt;
.clear {
    clear: both;
}
</code></pre>
  
The huge inconvenient of this technique is that you had to add an empty dividers after your floated elements to make it work.  
The [Micro Clearfix](http://nicolasgallagher.com/micro-clearfix-hack/) is now the most up-to-date best practice for clearing floats. It is supported by all modern browsers and by IE6 and up.  
The class is applied to the element that contains the floats. This way there is no more need for empty divs.  
```
.cf:before,
.cf:after {
    content: "";
    display: table;
}
.cf:after {
    clear: both;
}
.cf {
    *zoom: 1;
}
```

- **Image replacement**
An old technique to hide text from an element while keeping it accessible was to indent the text of -9999px. It is actually a bad practice beacause is creates a huge invisible box. Jeffrey Zeldman introduced the world to what he nicknamed the [Kellum Method](http://www.zeldman.com/2012/03/01/replacing-the-9999px-hack-new-image-replacement/) to a much better technique for the same effect.  
```
.hide-text {
    text-indent: 100%;
    white-space: nowrap;
    overflow: hidden;
}
```

###Text

- **Prefer ems to pixels**

- **Don't justify text**  
Justified text can generate readability issues by creating uneven spacing in paragraphs, particularly for Dyslexic users.

***

###Links

- **Specify a visited state**  
```
a:visited {
    color: red;
}
```

- **Don't underline something that isn't a link**  
Making something that isn't clickable look like it is causes frustration and confusion.  

***

###Forms 

- **Indicate when a form field is active**  
```
textarea:focus {  
    border: 1px solid red;
}
```

***

###Images

- **Make images fluid**  
Make images adapt with the size of their container. This way, images will shrink and grow within their container.  
```
img {
	max-width: 100%;
	height: auto;
}
```

- **Combine your images into sprite when possible**

***

###Background

- **Specify a background color when using background images**  
If you use a background image behind text, remember that the image might not load, or that the user can disable. Specifying a background color in the tones of the image might improve readability.  

*** 
Sources: [Line25](http://line25.com/articles/10-usability-crimes-you-really-shouldnt-commit), [Sitepoint](http://www.sitepoint.com/css-architectures-new-best-practices/), [Brian Gardner](http://www.briangardner.com/code/css-best-practices/), [Nettuts](http://net.tutsplus.com/tutorials/html-css-techniques/30-css-best-practices-for-beginners/)
