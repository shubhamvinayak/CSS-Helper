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
