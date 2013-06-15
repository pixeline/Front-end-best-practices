###General  

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

- **Use CSS3 techniques**
A lot of CSS3 properties can be used right now. 


- **Compress your CSS when you're done**  
A compressed file is smaller, thus faster to load.  
You can use [CSS Optimiser](http://www.cssoptimiser.com/), [CSS compressor](http://www.cssdrive.com/index.php/main/csscompressor/), [Clean CSS](http://www.cleancss.com/)  

- **Style all elements !**  
You might not need a blockquote at first launch, but that doesn't mean it won't ever be needed. Plan for every possible case !  
***

###Utilities  

- **Use the Micro Clearfix**  
This method has been used for a while to clear floats:  

```
div class="clear"></div>
.clear {
	clear: both;
}
```  

It's huge inconvenient is that you had to add an empty dividers after your floated elements to make it work.  
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

###Background

- **Specify a background color when using background images**  
If you use a background image behind text, remember that the image might not load, or that the user can disable. Specifying a background color in the tones of the image might improve readability.  

*** 
Sources: [Line25](http://line25.com/articles/10-usability-crimes-you-really-shouldnt-commit), [Sitepoint](http://www.sitepoint.com/css-architectures-new-best-practices/)