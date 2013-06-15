#HTML best practices

###Doctype 

- **Always use the HTML5 doctype**  
```
<!DOCTYPE html>  
```  
Sources: [Henri Sivonen](http://hsivonen.iki.fi/doctype/), [John Resig](http://ejohn.org/blog/html5-doctype/)

***  

###Head

- **Use meaningful title tags**  
The title tag appears in the browser tabs and in search engines' results. Make them helpful for understanding the content of your page.  

- **Use good meta tags**  
For example the 'description' meta, is about the purpose of your site and shows up in search engines' results.  

- **Place your stylesheets at the end of the Head tag**  
It allows the page to render progressively. The purpose is to make the page load look faster.

***

###Tags

- **Don't catch divitis**  
Many sites use way too many divs. Divs are meaningless elements that should be used as "elements of last resort when no other elements are suitable". You can probably cut some of these away while keeping a clean structure.  

- **If building a content site, save your h1 for article titles**  
It is common practice to use the h1 for the logo, but for SEO purposes, it's best it to use for article titles.  

- **Place your navigation inside unordered lists**  

- **Use an 'alt' attribute on all images**  
It is actually very important for accessibility and validation reasons.  

- **Use title attributes on links when it's relevant**  
Title attributes are read by screenreaders and should provide useful additional information.   

- **Don't place block elements inside inline elements**  
```
Don't do this: 
<a href="#"><h1>Wrong</h1></a>
Do that instead: 
<h1><a href="#">Right</a></h1>
```

- **Use label tags and associate them with their input**  
```
<label for="name">Name</label>
<input type="text" id="name">
```

- **Don't use ```<b>``` or ```<i>```**  
Use ```<strong>``` or ```<em>``` instead.  

- **Try not to use ```<br>```**  
Don't use it for presentation purposes. If you need to create gaps within a text, use multiple ```<p>``` instead.

- **Learn your tags**  
Some tags are often left unused and misundestood, but are quite useful in some situations.  
Don't leave out [cite](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/cite), [optgroup](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/optgroup), [ins](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ins), [del](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/del), [fieldset](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/fieldset), [abbr](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/abbr), etc.
Styles

***

###General

- **Be consistent**  
Be professional when writing your code from the start, indent it properly, and make it easy to read. Consider other people that might work on your code.  

***

###Scripts

- **Consider placing Javascript files at the end, just before the end of the body tag**  
When loading a script, the browser stops until the entire file has been loaded. The user won't notice any loading progress.  

- **Never, ever use inline Javascript**  
Keep your HTML clean.  

- **Compress your Javascript**  
You can user [Javascript Compressor](http://javascriptcompressor.com/), [JS Compressor](http://www.xmlforasp.net/JSCompressor.aspx)  

*** 

Main sources: [Nettuts](http://net.tutsplus.com/tutorials/html-css-techniques/30-html-best-practices-for-beginners/), [Nettuts](http://net.tutsplus.com/articles/web-roundups/10-rare-html-tags-you-really-should-know/), [SixRevisions](http://sixrevisions.com/web-standards/20-html-best-practices-you-should-follow/), [Line25](http://line25.com/articles/10-html-tag-crimes-you-really-shouldnt-commit)