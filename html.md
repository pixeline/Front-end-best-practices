#HTML best practices

###Doctype 
- **Always use the HTML5 doctype**  
```
<!DOCTYPE html>  
```  
Sources: [Henri Sivonen](http://hsivonen.iki.fi/doctype/), [John Resig](http://ejohn.org/blog/html5-doctype/)

***  

###Tags
- **Don't catch divitis**  
Many sites use way too many divs. You can probably cut some of these away while keeping a clean structure.  

- **If building a content site, save your h1 for article titles**  
It is common practice to use the h1 for the logo, but for SEO purposes, it's best it to use for article titles.  

- **Place your navigation inside unordered lists**  

- **Use an 'alt' attribute on all images**  
It is actually very important for accessibility and validation reasons.  

- **Learn your tags**  
Some tags are often left unused and misundestood, but are quite useful in some situations.  
Don't leave out [cite](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/cite), [optgroup](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/optgroup), [ins](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ins), [del](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/del), [fieldset](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/fieldset), [abbr](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/abbr), etc.



***  

###
- **Place all your styles before the end of the Head tag**  
It allows the page to render progressively. The purpose is to make the page load look faster.  

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
You can use [CSS Optimiser](http://www.cssoptimiser.com/), [CSS compressor](http://www.cssdrive.com/index.php/main/csscompressor/), [Clean CSS](http://www.cleancss.com/)  

- **Style all elements !**  
You might not need a blockquote at first launch, but that doesn't mean it won't ever be needed. Plan for every possible case !  

***  

###Scripts
- **Consider placing Javascript files at the end, just before the end of the body tag**  
When loading a script, the browser stops until the entire file has been loaded. The user won't notice any loading progress.  

- **Never, ever use inline Javascript**  
Keep your HTML clean.  

- **Compress your Javascript**  
You can user [Javascript Compressor](http://javascriptcompressor.com/), [JS Compressor](http://www.xmlforasp.net/JSCompressor.aspx)  

*** 
Sources used: [Nettuts](http://net.tutsplus.com/tutorials/html-css-techniques/30-html-best-practices-for-beginners/), [Nettuts](http://net.tutsplus.com/articles/web-roundups/10-rare-html-tags-you-really-should-know/)