#HTML best practices

## General

- **Be consistent**  
Be professional when writing your code from the start. Indent it properly, make it easy to read, be proud of the quality of your code. Consider other people that will work on your code.  

***

## Doctype 

- **Always use the HTML5 Doctype**  
```
<!DOCTYPE html>  
```  
Being the most up-to-date Doctype, it will stay this way for a very long time, ensuring the longevity of your page. All browsers will just render the page in "Standards mode", even if they don't support HTML5 features.

***  

## Head

- **Use meaningful title tags**  
The title tag appears in the browser's tabs and in search engines' results. They should help determine what the page is about at a glance.  
A few tips: keep it less than 70 characters long, use keywords at the beginning, use pipes | to separate phrases, leave out unimportant words, put your company/agency/person/... name at the end, use a different title tag on each page.  

- **Use good meta tags**  
Meta tags are mostly used by search engines and can be very powerful if used properly.  
How to use those meta tags in the best way possible isn't in the scope of this document, but I would recommend using these ones: [description](http://econsultancy.com/be/blog/62553-33-examples-of-great-meta-descriptions-for-search), [author](http://www.webmarketingnow.com/tips/meta-tags-meta-author.html), [robots](https://developers.google.com/webmasters/control-crawl-index/docs/robots_meta_tag), [opengraph](http://davidwalsh.name/facebook-meta-tags). 

- **Place your stylesheets at the end of the Head tag**  
Being at the top, CSS will be loaded first, allowing the page to render progressively. The purpose is to make the page load look faster.

***

## Tags

- **Stay way from divitis**  
Divs are meaningless elements that should be used as "elements of last resort when no other elements are suitable". You can probably cut some of these away while keeping a clean structure.

- **If building a content site, save your h1 for article titles**  
It is common practice to use the h1 for the logo, but for SEO purposes, it's best it to use for article titles.  

- **Place your navigation inside unordered lists**  
Research conducted by [Bruce Lawson](http://www.brucelawson.co.uk/2005/navigation-lists/), in 2005, concluded that it was best for accessibility and markup.

- **Use an `alt` attribute on all images**  
It is important for accessibility and validation reasons. The alt attribute will show if the image cannot be desplayed and will be read to screenreaders.   

- **Use `title` attributes on links when it's relevant**  
Do not duplicate the content of your link in the title attribute. It is there to provide additional information. 

- **Don't place block elements inside inline elements**  
```  
Wrong way:  
<a href="#"><h1>Title</h1></a>  
Right way:
<h1><a href="#">Title</a></h1>
```

- **Use label tags and associate them with their input**  
```
<label for="name">Name</label>
<input type="text" id="name">
```

- **Don't use `<b>` or `<i>`**  
Use `<strong>` or `<em>` instead.  

- **Try not to use `<br>`**  
Don't use it for presentation purposes. If you need to create gaps within a text, use multiple `<p>` instead.

- **Learn your tags**  
Some tags are often left unused and misundestood, but are quite useful in some situations.  
Don't leave out [cite](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/cite), [optgroup](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/optgroup), [ins](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ins), [del](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/del), [fieldset](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/fieldset), [abbr](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/abbr), etc.

***

## Scripts

- **Consider placing Javascript files at the end, just before the end of the body tag**  
When loading a script, the browser stops until the entire file has been loaded. The user won't notice any loading progress.  

- **Never, ever use inline Javascript**  
Keep your HTML clean.  

- **Compress your Javascript**  
You can user [Javascript Compressor](http://javascriptcompressor.com/), [JS Compressor](http://www.xmlforasp.net/JSCompressor.aspx)  

*** 

Main sources: [Nettuts](http://net.tutsplus.com/tutorials/html-css-techniques/30-html-best-practices-for-beginners/), [Nettuts](http://net.tutsplus.com/articles/web-roundups/10-rare-html-tags-you-really-should-know/), [SixRevisions](http://sixrevisions.com/web-standards/20-html-best-practices-you-should-follow/), [Line25](http://line25.com/articles/10-html-tag-crimes-you-really-shouldnt-commit), [Search Engine Land](http://searchengineland.com/writing-html-title-tags-humans-google-bing-59384), [iacquire](http://www.iacquire.com/blog/18-meta-tags-every-webpage-should-have-in-2013/)