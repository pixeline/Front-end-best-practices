#HTML best practices

###Doctype 
- Always use the HTML5 doctype
```
<!DOCTYPE html>
```
Sources: [Henri Sivonen](http://hsivonen.iki.fi/doctype/), [John Resig](http://ejohn.org/blog/html5-doctype/)

***
###Tags
- If building a content site, save your <h1> for article titles  
It is common practice to use the <h1> for the logo, but for SEO purposes, it's best to use for article titles.  

- Place your navigation inside unordered lists 

***

###Styles
- Place all your styles before the end of the Head tag  
It allows the page to render progressively. The purpose is to make the page load look faster.  

- Never use inline styles  
Keep the styles out of the HTML. Think separation of concerns. It makes mainteanance much easier.  

- Target IE with specific stylesheets  
```
<!--[if lt IE 7] >
	<link rel="stylesheet" href="ie.css">
<![endif]-->
```

*** 

###Scripts
- Consider placing Javascript files at the end, just before the end of the body tag  
When loading a script, the browser stops until the entire file has been loaded. The user won't notice any loading progress.  

- Never, ever use inline Javascript  
Keep your HTML clean. 

*** 
Sources used: [Nettuts](http://net.tutsplus.com/tutorials/html-css-techniques/30-html-best-practices-for-beginners/)