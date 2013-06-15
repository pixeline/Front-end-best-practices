###Text

- **Don't justify text**  
Justified text can generate readability issues by creating uneven spacing in paragraphs, particularly for Dyslexic users.

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
Sources: [Line25](http://line25.com/articles/10-usability-crimes-you-really-shouldnt-commit)