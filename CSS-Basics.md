https://github.com/learning-zone/css-interview-questions

## Box model
![image](https://user-images.githubusercontent.com/45894327/121133016-783a7280-c84f-11eb-9d99-44c962202c28.png)

### width and height
Box Size	CSS Properties

Total Width: 	width + padding-left + padding-right + border-left + border-right + margin-left + margin-right

Total Height:	height + padding-top + padding-bottom + border-top + border-bottom + margin-top + margin-bottom.

The width and height property defines the width and height of the content area of an element.

You can use the max-width and max-height property to specify the maximum width and height of the content area. This maximum width and height does not include paddings, borders, or margins. Likewise, an element that has max-height applied will never be taller than the value specified, even if the height property is set to something larger. For example, if the height is set to 200px and the max-height set to 100px, the actual height of the element will be 100px.

You can use the min-width and min-height property specify the minimum width and height of the content area. This minimum width and height does not include paddings, borders, or margins.An element cannot be narrower than the min-width value, even if the width property value is set to something lesser. For example, if the width is set to 300px and the min-width is set to 400px, the actual width of the element will be 400px. Let's see how it actually works:

### Padding:
The CSS padding properties allow you to set the spacing between the content of an element and its border (or the edge of the element's box, if it has no defined border).
You can specify the paddings for the individual sides of an element such as top, right, bottom, and left sides using the CSS padding-top, padding-right, padding-bottom, and the padding-left properties, respectively. 
```html
padding: 50px; /* apply to all four sides */
padding: 25px 75px; /* vertical | horizontal */
padding: 25px 50px 75px; /* top | horizontal | bottom */
padding: 25px 50px 75px 100px; /* top | right | bottom | left */
```

* Effect of Padding and Border on Layout
if you set the width of a <div> element to 100% and also apply left right padding or border on it, the horizontal scrollbar will appear. Let's see an example:
```html
  div {
    width: 100%;
    padding: 25px;
}
```
To prevent padding and border from changing element's box width and height, you can use the CSS box-sizing property.
```html
div {
    width: 100%;
    padding: 25px;
    box-sizing: border-box;
}
```
  
### Border
* The border-style property can have the following values: none, hidden, solid, dashed, dotted, double, inset, outset, groove, and ridge. The values none and hidden displays no border, however, there is a slight difference between these two values. In the case of table cell and border collapsing, the none value has the lowest priority, whereas the hidden value has the highest priority, if any other conflicting border is set.
* The border-width property specifies the width of the border area. It is a shorthand property for setting the thickness of all the four sides of an element's border at the same time.
* The border-color property specifies the color of the border area. This is also a shorthand property for setting the color of all the four sides of an element's border.
* The Border Shorthand Property : border: 5px solid #00ff00;
  
### CSS-Margin
The CSS margin properties allow you to set the spacing around the border of an element's box (or the edge of the element's box, if it has no defined border).
* You can specify the margins for the individual sides of an element such as top, right, bottom, and left sides using the CSS margin-top, margin-right, margin-bottom, and the margin-left properties, respectively. Let's try out the following example to understand how it works:
```html
 margin: 50px; /* apply to all four sides */
 margin: 25px 75px; /* vertical | horizontal */
 margin: 25px 50px 75px; /* top | horizontal | bottom */
 margin: 25px 50px 75px 100px; /* top | right | bottom | left */
```
* Horizontal Centering with Auto Margins: 
 ```html
div {
    width: 300px;
    background: gray;
    margin: 0 auto;
}
```
-----------------------------------------------------------------------------------------------------------------------------
###  Q. What is the difference between padding and margin
1) Margin is applied to the outside of you element hence effecting how far your element is away from other elements.
2) Padding is applied to the inside of your element hence effecting how far your element's content is away from the border.

Also, using margin will not affect your element's dimensions whereas padding will make your elements dimensions (set height + padding) so for example if you have a 100x100px div with a 5 px padding, your div will actually be 105x105px.
  ![image](https://user-images.githubusercontent.com/45894327/121137084-f26cf600-c853-11eb-8b0b-368bff25b0bf.png)

<p>Note- Top/Bottom margins are collapsible: if you have a 20px margin at the bottom of an element and a 30px margin at the top of the next element, the margin between the two elements will be 30px rather than 50px. This does not apply to left/right margin or padding.</p>
  
--------------------------------------------------------------------------------------------------------------------------------------------------
### Q.What is the purpose of the box-sizing property?
  The box-sizing CSS property sets how the total width and height of an element is calculated.

content-box: the default width and height values apply to the element's content only. The padding and border are added to the outside of the box.
padding-box: Width and height values apply to the element's content and its padding. The border is added to the outside of the box. Currently, only Firefox supports the padding-box value.
border-box: Width and height values apply to the content, padding, and border.
inherit: inherits the box sizing of the parent element.
```html
box-sizing: content-box;
width: 100%;
border: solid rgb(90,107,204) 10px;
padding: 5px;
```
  ---------------------------------------------------------------------------------------------------------------------
### Basics- CSS selector
![image](https://user-images.githubusercontent.com/45894327/121138058-f2b9c100-c854-11eb-9bcf-8604144367d6.png)
A CSS selector is the part of a CSS rule set that actually selects the content you want to style.
i) Universal Selector: The universal selector works like a wild card character, selecting all elements on a page. Every HTML page is built on content placed within HTML tags. Each set of tags represents an element on the page.
 ```html
 * {
   color: green;
   font-size: 20px;
   line-height: 25px;
}
```
ii) Element Type Selector: This selector match one or more HTML elements of the same name.
```html
ul {
   list-style: none;
   border: solid 1px #ccc;
}
<ul>
  <li>Fish</li>
  <li>Apples</li>
  <li>Cheese</li>
</ul>

<div class="example">
  <p>Example paragraph text.</p>
</div>

<ul>
  <li>Water</li>
  <li>Juice</li>
  <li>Maple Syrup</li>
</ul>

```
iii) ID Selector: This selector matches any HTML element that has an ID attribute with the same value as that of the selector.
```html
#container {
   width: 960px;
   margin: 0 auto;
}
<div id="container"></div>
```
iv) Class Selector: The class selector also matches all elements on the page that have their class attribute set to the same value as the class.
```html
.box {
   padding: 20px;
   margin: 10px;
   width: 240px;
}
<div class="box"></div>
```
v) Descendant Combinator: The descendant selector or, more accurately, the descendant combinator lets you combine two or more selectors so you can be more specific in your selection method.
```html
#container .box {
   float: left;
   padding-bottom: 15px;
}
```
This declaration block will apply to all elements that have a class of box that are inside an element with an ID of container. It’s worth noting that the .box element doesn’t have to be an immediate child: there could be another element wrapping .box, and the styles would still apply.
```html
<div id="container">
  <div class="box"></div>

  <div class="box-2"></div>
</div>

<div class="box"></div>
```
vi) Child Combinator: A selector that uses the child combinator is similar to a selector that uses a descendant combinator, except it only targets immediate child elements.
```html
#container > .box {
   float: left;
   padding-bottom: 15px;
}
```
The selector will match all elements that have a class of box and that are immediate children of the #container element. That means, unlike the descendant combinator, there can’t be another element wrapping .box—it has to be a direct child element.
```html
<div id="container">
  <div class="box"></div>

  <div>
    <div class="box"></div>
  </div>
</div>
```
vii) General Sibling Combinator: A selector that uses a general sibling combinator matches elements based on sibling relationships. The selected elements are beside each other in the HTML.
```html
h2 ~ p {
   margin-bottom: 20px;
}
```
In this example, all paragraph elements (`<p>`) will be styled with the specified rules, but only if they are siblings of `<h2>` elements. There could be other elements in between the `<h2>` and `<p>`, and the styles would still apply.
```html
<h2>Title</h2>
<p>Paragraph example.</p>
<p>Paragraph example.</p>
<p>Paragraph example.</p>
<div class="box">
  <p>Paragraph example.</p>
</div>
```
viii) Adjacent Sibling Combinator: A selector that uses the adjacent sibling combinator uses the plus symbol (+), and is almost the same as the general sibling selector. The difference is that the targeted element must be an immediate sibling, not just a general sibling.
```html
p + p {
   text-indent: 1.5em;
   margin-bottom: 0;
}
```
In this example will apply the specified styles only to paragraph elements that immediately follow other paragraph elements. This means the first paragraph element on a page would not receive these styles. Also, if another element appeared between two paragraphs, the second paragraph of the two wouldn’t have the styles applied.
```html
<h2>Title</h2>
<p>Paragraph example.</p>
<p>Paragraph example.</p>
<p>Paragraph example.</p>

<div class="box">
  <p>Paragraph example.</p>
  <p>Paragraph example.</p>
</div>
```
ix) Attribute Selector: The attribute selector targets elements based on the presence and/or value of HTML attributes, and is declared using square brackets
 ```html
input[type="text"] {
   background-color: #444;
   width: 200px;
}
<input type="text">
```
The attribute selector can also be declared using just the attribute itself, with no value, like this:
```html
input[type] {
   background-color: #444;
   width: 200px;
}
```
x) Pseudo-class: A pseudo-class uses a colon character to identify a pseudo-state that an element might be in—for example, the state of being hovered, or the state of being activated.
```html
a:hover {
   color: red;
}
```
xi) Pseudo-element: A CSS pseudo-element is used to style specified parts of an element. For example, it can be used to:
Style the first letter, or line, of an element
Insert content before, or after, the content of an element
```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      p::first-line {
        color: #ff0000;
        font-variant: small-caps;
      }

      p::first-letter {
        color: #ff0000;
        font-size: xx-large;
      }

      h1::before {
        content: url(smiley.gif);
      }

      h1::after {
        content: url(smiley.gif);
      }

      ::selection {
        color: red;
        background: yellow;
      }
    </style>
  </head>
<body>
  <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry.
  Lorem Ipsum has been the industry\'s standard dummy text ever since the 1500s,
  <h1>when an unknown printer took a galley of type and scrambled it to make a
  type specimen book.<h1></p>
</body>
</html>
```
xii)contextual selector:Contextual selector addresses specific occurrence of an element. It is a string of individual selectors separated by white space (search pattern), where only the last element in the pattern is addressed providing it matches the specified contex.
It also check the context of the class in the html tree, assigning the style to the element through a specific route, taking into account the order of depth in the tree.
Example:

table p { property: value; } 
----------------------------------------------------------------------------------------------------------------------------------------------------
### Q.What is the difference between class selectors and id selectors
In the CSS, a class selector is a name preceded by a full stop (“.”) and an ID selector is a name preceded by a hash character (“#”). The difference between an ID and a class is that an ID can be used to identify one element, whereas a class can be used to identify more than one.
```html
#top {
    background-color: #ccc;
    padding: 20px
}

.intro {
    color: red;
    font-weight: bold;
}
```
```html
<div id="top">

<h1>Chocolate curry</h1>
<p class="intro">This is my recipe for making curry purely with chocolate</p>
<p class="intro">Mmm mm mmmmm</p>

</div>
```
------------------------------------------------------------------------------------------------------------------------------------------------
### CSS position Property
absolute, place an element exactly where you want to place it. absolute position is actually set relative to the element's parent. if no parent available then relatively place to the page itself (it will default all the way back up to the element).

relative, means "relative to itself". Setting position: relative; on an element and no other positioning attributes, it will no effect on it's positioning. It allows the use of z-index on the element and it limits the scope of absolutely positioned child elements. Any child element will be absolutely positioned within that block.

fixed, element is positioned relative to viewport or the browser window itself. viewport doesn't changed if you scroll and hence fixed element will stay right in the same position.

static default for every single page element. The only reason you would ever set an element to position: static is to forcefully-remove some positioning that got applied to an element outside of your control.

<p>sticky - Sticky positioning is a hybrid of relative and fixed positioning. The element is treated as relative positioned until it crosses a specified threshold, at which point it is treated as fixed positioned.</p>
  
![image](https://user-images.githubusercontent.com/45894327/121157241-0110d880-c867-11eb-99cc-21d0aeb1c2f9.png)
----------------------------------------------------------------------------------------------------------------------------------------------------
### block, inline and inline-block element
a) Block Elements
The block elements always start on a new line. They will also take space of an entire row or width. List of block elements are `<p>, <h1>, <div>, <header>`.

Example:
```html
 <p>
  Lorem ipsum dolor sit amet consectetur adipisicing elit. Unde autem,
  consequatur deleniti nobis beatae quo dolore nemo corporis. Ad delectus
  dignissimos pariatur illum eveniet dolor rem eius laborum sed iure!
</p>

<p>
  Lorem ipsum dolor sit amet consectetur adipisicing elit. Unde autem,
  consequatur deleniti nobis beatae quo dolore nemo corporis. Ad delectus
  dignissimos pariatur illum eveniet dolor rem eius laborum sed iure!
</p>
```
b) Inline Elements
Inline elements don't start on a new line, they appear on the same line as the content and tags beside them. Some examples of inline elements are `<a>, <span> , <strong>, and <img> tags`.

When it comes to margins and padding, browsers treat inline elements differently. You can add space to the left and right on an inline element, but you cannot add height to the top or bottom padding or margin of an inline element.

Example:
```html
<a href="#">Link</a>
<img src="https://picsum.photos/30" />
<span>Span</span>
<strong>Strong Player</strong>
```
c) Inline-Block Elements
Inline-block elements are similar to inline elements, except they can have padding and margins added on all four sides. One common use for using inline-block is for creating navigation links horizontally. Some examples of inline-block elements are `<input>, <button>, <select>, <textarea>` etc.
```html
input {
  width: 300px;
  height: 50px;
}

button {
  width: 100px;
  height: 50px;
  margin-top: 20px;
}

<input type="text" /> <button>Submit</button>
```
-----------------------------------------------------------------------------------------------------------------------------------------------------------
###  pseudo element and  pseudo class

For example, it can be used to:

* Style the first letter, or line, of an element
* Insert content before, or after, the content of an element

**CSS Pseudo Elements**  

|Sl.No|Selector	      |Example	        |description|
|-----|---------------|-----------------|-------------|
| 01. |::after	      |p::after	        |Insert something after the content of each <p> element|
| 02. |::before	      |p::before	      |Insert something before the content of each <p> element|
| 03. |::first-letter	|p::first-letter	|Selects the first letter of each <p> element|
| 04. |::first-line	  |p::first-line	  |Selects the first line of each <p> element|
| 05. |::selection	  |p::selection	    |Selects the portion of an element that is selected by a user|


**2. Pseudo-classes**: A pseudo-class is used to define a special state of an element.

For example, it can be used to:

* Style an element when a user mouses over it
* Style visited and unvisited links differently
* Style an element when it gets focus

**CSS Pseudo Classes**  

| Sl.No |Selector	         | Example	              |description|
|-------|------------------|------------------------|-----------|
| 01.  |:active	           |a:active	              |Selects the active link|
| 02.  |:checked	         |input:checked	          |Selects every checked `<input>` element|
| 03.  |:disabled	         |input:disabled	        |Selects every disabled `<input>` element|
| 04.  |:empty	           |p:empty	                |Selects every `<p>` element that has no children|
| 05.  |:enabled	         |input:enabled	          |Selects every enabled `<input>` element|
| 06.  |:first-child	     |p:first-child	          |Selects every `<p>` elements that is the first child of its parent|
| 07.  |:first-of-type	   |p:first-of-type	        |Selects every `<p>` element that is the first `<p>` element of its parent|
| 08.  |:focus	           |input:focus	            |Selects the `<input>` element that has focus|
| 09.  |:hover	           |a:hover	                |Selects links on mouse over|
| 10.  |:in-range	         |input:in-range	        |Selects `<input>` elements with a value within a specified range|
| 11.  |:invalid	         |input:invalid	          |Selects all `<input>` elements with an invalid value|
| 12.  |:lang(language)	   |p:lang(it)	            |Selects every `<p>` element with a lang attribute value starting with "it"|
| 13.  |:last-child	       |p:last-child	          |Selects every `<p>` elements that is the last child of its parent|
| 14.  |:last-of-type	     |p:last-of-type	        |Selects every `<p>` element that is the last `<p>` element of its parent|
| 15.  |:link	             |a:link	                |Selects all unvisited links|
| 16.  |:not(selector)	   |:not(p)	                |Selects every element that is not a `<p>` element|
| 17.  |:nth-child(n)	     |p:nth-child(2)	        |Selects every `<p>` element that is the second child of its parent|
| 18.  |:nth-last-child(n) |p:nth-last-child(2)	    |Selects every `<p>` element that is the second child of its parent, |counting from the last child|
| 19.  |:nth-last-of-type(n) |p:nth-last-of-type(2)	|Selects every `<p>` element that is the second `<p>` element of its parent, counting from the last child|
| 20.  |:nth-of-type(n)	    |p:nth-of-type(2)	      |Selects every `<p>` element that is the second `<p>` element of its parent|
| 21.  |:only-of-type	      |p:only-of-type	        |Selects every `<p>` element that is the only `<p>` element of its parent|
| 22.  |:only-child	        |p:only-child	          |Selects every `<p>` element that is the only child of its parent|
| 23.  |:optional	          |input:optional	        |Selects `<input>` elements with no "required" attribute|
| 24.  |:out-of-range	      |input:out-of-range	    |Selects `<input>` elements with a value outside a specified range|
| 25.  |:read-only	        |input:read-only	      |Selects `<input>` elements with a "readonly" attribute specified|
| 26.  |:read-write	        |input:read-write	      |Selects `<input>` elements with no "readonly" attribute|
| 27.  |:required	          |input:required	        |Selects `<input>` elements with a "required" attribute specified|
| 28.  |:root	root	        |                       |Selects the document\'s root element|
| 29.  |:target	            |#news:target	          |Selects the current active #news element (clicked on a URL containing that anchor name)|
| 30.  |:valid	            |input:valid	          |Selects all `<input>` elements with a valid value|
| 31.  |:visited	          |a:visited	            |Selects all visited links|

 ----------------------------------------------------------------------------------------------------------------------------------------------------
### Float
  
  The float CSS property places an element on the left or right side of its container, allowing text and inline elements to wrap around it. are not  absolutely positioned. which means that an element can only be floated left or right, not up or down.

**Syntax**  
```css
/* Keyword values */
float: left;
float: right;
float: none;
float: inline-start;
float: inline-end;

/* Global values */
float: inherit;
float: initial;
float: unset;
```
**Property Values**  

|Sl.No| Value  | Description| 
|-----|--------|------------|
| 01. |none	   |The element does not float, (will be displayed just where it occurs in the text).|	
| 02. |left	   |The element floats to the left of its container	|
| 03. |right	 |The element floats the right of its container	|
| 04. |initial |Sets this property to its default value.    	|
| 05. |inherit |Inherits this property from its parent element. |

Example:
```css
section {
  border: 1px solid blue;
  width: 100%;
  float: left;
}

div {
  margin: 5px;
  width: 50px;
  height: 150px;
}

.left {
  float: left;
  background: pink;
}

.right {
  float: right;
  background: cyan;
}
```
```html
<section>
  <div class="left">1</div>
  <div class="left">2</div>
  <div class="right">3</div>
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.
     Morbi tristique sapien ac erat tincidunt, sit amet dignissim
     lectus vulputate. Donec id iaculis velit. Aliquam vel
     malesuada erat. Praesent non magna ac massa aliquet tincidunt
     vel in massa. Phasellus feugiat est vel leo finibus congue.</p>
</section>
```
....
Clear property:
Elements that comes after the floating element will flow around it. The clear property specifies which sides of an element's box other floating elements are not allowed.

|Sl.No| Properties     | Description  |
|-----|----------------|--------------|
| 01. |clear: none     |Allows floating elements on both sides. This is default|
| 02. |clear: left     |No floating elements allowed on the left side|
| 03. |clear: right    |No floating elements allowed on the right side|
| 04. |clear: both     |No floating elements allowed on either the left or the right side|
| 05. |clear: inherit  |The element inherits the clear value of its parent|

Example
```css
div {
  clear: left;
}
```
------------------------------------------------------------------------------------------------------------------------------------------------------
### Display Property

The display property specifies the display behavior (the type of rendering box) of an element.  
Example:
```css
p.ex1 {display: none;}
p.ex2 {display: inline;}
p.ex3 {display: block;}
p.ex4 {display: inline-block;}
```

**Property Values**  

|Sl.No|Value	   |Description	
|-----|---------------|------------------
| 01. |inline	|Displays an element as an inline element (like `<span>`). Any height and width properties will have no effect|	
| 02. |block	|Displays an element as a block element (like `<p>`). It starts on a new line, and takes up the whole width	|
| 03. |contents|Makes the container disappear, making the child elements children of the element the next level up in the DOM	|
| 04. |flex	          |Displays an element as a block-level flex container	|
| 05. |grid	          |Displays an element as a block-level grid container	|
| 06. |inline-block   |Displays an element as an inline-level block container. The element itself is formatted as an inline element, but you can apply height and width values|	
| 07. |inline-flex	   |Displays an element as an inline-level flex container	|
| 08. |inline-grid	   |Displays an element as an inline-level grid container	|
| 09. |inline-table    |The element is displayed as an inline-level table	|
| 10. |list-item	     |Let the element behave like a `<li>` element	|
| 11. |run-in	         |Displays an element as either block or inline, depending on context	|
| 12. |table	         |Let the element behave like a `<table>` element	|
| 13. |table-caption	 |Let the element behave like a `<caption>` element	|
| 14. |table-column-group	|Let the element behave like a `<colgroup>` element	|
| 15. |table-header-group	|Let the element behave like a `<thead>` element	|
| 16. |table-footer-group	|Let the element behave like a `<tfoot>` element	|
| 17. |table-row-group	  |Let the element behave like a `<tbody>` element	|
| 18. |table-cell	        |Let the element behave like a `<td>` element	|
| 19. |table-column	      |Let the element behave like a `<col>` element	|
| 20. |table-row	        |Let the element behave like a `<tr>` element	|
| 21. |none	              |The element is completely removed	|
| 22. |initial	          |Sets this property to its default value. Read about initial	|
| 23. |inherit	          |Inherits this property from its parent element. Read about inherit|
---------------------------------------------------------------------------------------------------------------------------------------------
### Visibilty of Element
You can use the visibility property to control whether an element is visible or not. This property can take one of the following values listed in the table below:
  
visible:	Default value. The box and its contents are visible.
  
hidden:	The box and its content are invisible, but still affect the layout of the page.
  
collapse:	This value causes the entire row or column to be removed from the display. This value is used for row, row group, column, and column group elements.
  
inherit:	Specifies that the value of the visibility property should be inherited from the parent element i.e. takes the same visibility value as specified for its parent.
  
visibility: hidden simply hides the element but it will occupy space and affect the layout of the document.
  
display: none removes the element from the normal layout flow (causes DOM reflow). It will not affect the layout of the document nor occupy space.
  
------------------------------------------------------------------------------------------------------------------------------------------------------------
 
 ### CSS Opacity
  
![image](https://user-images.githubusercontent.com/45894327/121169399-96b16580-c871-11eb-9901-c3cc86d8f2a4.png)

  
The `opacity` CSS property sets the opacity of an element. Opacity is the degree to which content behind an element is hidden, and is the opposite of transparency.

```css
div { background-color: lightblue; }
.light {
  opacity: 30%; /* Barely see the text over the background */
}
.medium {
  opacity: 60%; /* See the text more clearly over the background */
}
.heavy {
  opacity: 100%; /* See the text very clearly over the background */
}
```

```html
<div class="light">You can barely see this.</div>
<div class="medium">This is easier to see.</div>
<div class="heavy">This is very easy to see.</div>
```
-----------------------------------------------------------------------------------------------------------------------------------------------------------------
### OverFlow
There may be a situation when the content of an element might be larger than the dimensions of the box itself. For example given width and height properties did not allow enough room to accommodate the content of the element.
  
visible: The default value. Content is not clipped; it will be rendered outside the element's box, and may thus overlap other content.
  
hidden:	Content that overflows the element's box is clipped and the rest of the content will be invisible.
  
scroll:	The overflowing content is clipped, just like hidden, but provides a scrolling mechanism to access the overflowed content.
  
auto:	If content overflows the element's box it will automatically provides the scrollbars to see the rest of the content, otherwise scrollbar will not appear.
  
---------------------------------------------------------------------------------------------------------------------------------------------------------
  
### Z-Index:
  
 The z-index CSS property specifies the layering or stacking order for the positioned elements i.e. elements whose position value is one of absolute, fixed, or relative. The stacking order refers to the position of elements along the Z-axis which is perpendicular to the screen.
 `z-index: integer | auto | initial | inherit`
  
  `integer`	Sets the stack level of the element's box in the current stacking context. The box also establishes a local stacking context in which its stack level is 0 (zero). Negative integer values are allowed.
`auto`	The stack level of the element's box is the same as its parent's box, and doesn't establish a new stacking context. This is default value.
`initial`	Sets this property to its default value.
`inherit`	If specified, the associated element takes the computed value of its parent element z-index property.
  
 ----------------------------------------------------------------------------------------------------------------------------------------------------------
  
  

