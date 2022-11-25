# myJourneyToLearnWeb

### HTML Fundamentals 
-What is HTML? (Hyper text markup language)
-It's made up of tags
-elements of HTML are made up of opening tags e.g <p>...</p> 
-some tags dont need to be closed
check https://developer.mozilla.org/en-US/docs/Web/HTML/Element out 
---------------------------------------------------------------------
### The DOCTYPE
```HTML
<!DOCTYPE html>
```
DOCTYPE purpose is to tell the browser what version of HTML it should use to render the document
---------------------------------------------------------------------
### HTML element 
```HTML
<html lang="en">
</html>
```
the Root element of the document
language atrribute: specifes the language of the text content. making it easier on text reader for example
---------------------------------------------------------------------

### Head element 
```HTML
<head >
  <meta charset="utf-8">
</head>
```
in heead element we put important meta-info about our wepage
charset meta encoding element makes sure that displaying special charchters from differnt lnaguage correct 
---------------------------------------------------------------------
### Title element 
```HTML
<title>My First Webpage
</title>
```
this is the title that displayed in the web-browser tab
---------------------------------------------------------------------
### Body Element
```HTML
<body>

</body>
```
this is where all the content go!

#### inside the body
```<p> - Paragraph [simple paragraph] </p> 
<h1..h6> - Headings and the number represent the heading level </h1..h6> 
<strong> - Bold , really helpful for visual impairment </strong>
<em> - emphasis on the text  </em> 
```

---------------------------------------------------------------------
### nesting and indentation 

when we nest element we crate parent and a child code
---------------------------------------------------------------------
### comments 
```<!-- comment here -->```
---------------------------------------------------------------------
### Listsc
```<ul>- unordered lists
<ol>-ordered lists
<li> each item witin the list ```
many atrributes [start ="#number" , reversed, value=""]
another type is description list ``` <dl> <dt> <dd>```
it can be nested very usful!
list have many styles: https://learn.shayhowe.com/html-css/creating-lists/

---------------------------------------------------------------------
### Links and images
#### Links 
Anchor elements - ```<a>```
hyper link refrence -```herf attributes within the anchor```

absloute links--protocol://domain/path
relitive links-- links to other pages in our website
"pages/about.html"
"./pages/about.html" -- start looking from the current diractory 
#### images
```<img> - self closing
need src=""```
same linking princples apply [absloute and relitve]
alt attribute- alterintive text