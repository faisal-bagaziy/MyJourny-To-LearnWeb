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
### Lists
```<ul>- unordered lists
<ol>-ordered lists
<li> each item witin the list 
```
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
need src=""
```
same linking princples apply [absloute and relitve]
alt attribute- alterintive text

---------------------------------------------------------------------
# CSS
BASIC syntax selector {
  proprety: value;
}
comment 
```
/* comment */
```

```
Note:
A <div> is one of the basic HTML elements. It is simply an empty container. In general, it is best to use other tags such as <h1> or <p> for content in your projects, but as we learn more about CSS you’ll find that there are many cases where the thing you need is just a container for other elements. Many of our exercises use plain <div>s for simplicity. Later lessons will go into much more depth about when it is appropriate to use the various HTML elements.
```
## selector
selector is simply refrer to the HTML element the css rule apply
```
universal selectors: *asterisk 
type selectors: name of the element
class selector: .className
id selector: #idName
```
##### class vs id
an element can have one id and id should not contain anywhite space
##### grouping selectors 
```
nameofSelctor1,
 nameofSelctor2{
  property : values;
}
```
chaining selectors
chain selector as list
this better explained with example
```
<div>
  <div class="subsection header">Latest Posts</div>
  <p class="subsection preview">This is where a preview for a post might go.</p>
</div>

.subsection.header {
  color: red;
}

this also work if you want to chain class into id 

how does it work?
it just concatenate subsectionheader and try to find it  
.ancestor .child
no limit for this chain 
```

### some frequant properties of css
```
color - set a text color
background-color - set the background color
they accept {HEX, RGB, HSL, KEYWORDS}
```

typography and text-align
```
font-family - 
accept "font family name" or genric name font-name no white spaces
```

```
note: 
If a browser cannot find or does not support the first font in a list, it will use the next one, then the next one and so on until it finds a supported and valid font. This is why it’s best practice to include a list of values for this property, starting with the font you want to be used most and ending with a generic font family as a fallback, e.g. font-family: "Times New Roman", sans-serif;
```

```
font-size: valuepx
font-weight - affect the boldens of the text from 1 and 1000 , you can use the word bold which is equal to 700
text-align - center for example
```

images height and width

```
By default, an <img> element’s height and width values will be the same as the actual image file’s height and width. If you wanted to adjust the size of the image without causing it to lose its proportions, you would use a value of “auto” for the height property and adjust the width value:

img {
  height: auto;
  width: 500px;
}

For example, if an image’s original size was 500px height and 1000px width, using the above CSS would result in a height of 250px

```
## box-model
>Every single thing on a webpage is a rectangular box. 

### margin 
> increase size between box and its nighbors this sometime include the whole page
> https://css-tricks.com/almanac/properties/m/margin
### padding 
> increase the distance between the edge of box and its content
### border 
> add spaces between  margin and padding 

## block vs inline
> block elements will appear on the page stacked atop each other, each new element starting on a new line.
> Inline elements do not start on a new line. They appear in line with whatever elements they are placed beside.

## divs and spans 
> divs and spans give no particular meaning to their content. They are just generic boxes that can contain anything.
> Div is a block-level element by default. It is commonly used as a container element to group other elements. Divs allow us to divide the page into different blocks and apply styling to those blocks.
>Span is an inline-level element by default. It can be used to group text content and inline HTML elements for styling and should only be used when no other semantic HTML element is appropriate.

## normal flow 
https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Normal_Flow
## inline-block
https://www.digitalocean.com/community/tutorials/css-display-inline-vs-inline-block

## Flex box

> its a block elemets, container
> Display: flex; organize the elements left to right
> https://www.internetingishard.com/html-and-css/flexbox/
> justify-content: {center, flex-start, flex-end, space-around, space-between}

## flex

> this a shorthand for 3 properties of flex items
> These properties affect how flex items size themselves within their container.
> the propties are flex-grow, flex-shrink and flex-basis.

```
div {
  flex: 1;
}
```

> this will apply flex-grow: 1, flex-shrink: 1, flex-basis: 0.
> flex-grow: grow factor of flex items
> flex-shrink: grow not larger than [min], shrink flex item if its larger than flex container fr example. tells the browser what the minimum size of an element should be.
> flex-basis: take [ideal size] if not possible take up as much space proprtionally as it can
> flex: [max] [min] [ideal size]; is a good way to see this
> they all work togther!

## axis

> flex-direction
> the defualt is horizontal, Row.
> other possible value is column which is vertical direction
> when using column as value we cant use the shorthand flex:1; for example.
> when using column as value flex-basis refer to height not width.
> adding row-reverse, colmn-reverse make the items oppsite to its original

## allignment

### justify content [main axis] [x-axis]

> justify-content in the container with values{flex-start, flex-end, center, space-between, space-around, sapce-evenly}

### align items [cross axis] [y-axis]

> align-items in container with values {flex-start, flex-end, center, baseline, stretch}
> note: when you change flex-direction to column justify content will take corss axis [y-axis] and align items take main axis [x-axis]

### allign self

> align-self:

### gap

> gap on a flex container simply adds a specified space between flex items


