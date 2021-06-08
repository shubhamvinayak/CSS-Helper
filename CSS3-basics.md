### Basics
https://www.tutorialrepublic.com/css-tutorial/css3-border.php

### Border
* The `border-radius` property can be used to create rounded corners. `border-radius: 20px;`
* The `border-image` property allows you to specify an image to act as an element's border. `border-image: url("border.png") 30 30 round;`

### Color
* Colors can be defined in the RGBA model (red-green-blue-alpha) using the rgba() functional.The alpha parameter accepts a value from 0.0 (fully transparent) to 1.0 (fully opaque).
`color: rgba(0,0,255,0.5);`
* Colors also can be defined the HSL model (hue-saturation-lightness) using the hsl() functional notation. Hue is represented as an angle (from 0 to 360) of the color wheel or circle (i.e. the rainbow represented in a circle). This angle is given as a unit less number because the angle is so typically measured in degrees that the unit is implicit in CSS.Saturation and lightness are represented as percentages. 100% saturation means full color, and 0% is a shade of gray. Whereas, 100% lightness is white, 0% lightness is black, and 50% lightness is normal.
`color: hsl(360,70%,60%);`
* Colors can be defined in the HSLA model (hue-saturation-lightness-alpha) using the hsla() functional notation. HSLA color model are an extension of HSL color model with an alpha channel — which specifies the opacity of a color.
The alpha parameter accepts a value from 0.0 (fully transparent) to 1.0 (fully opaque).`color: hsla(360,80%,50%,0.5);`

### Background
* The background-size property can be used to specify the size of the background images.  Prior to CSS3, the size of the background images was determined by the actual size of the images. The background image size can be specified using the pixels or percentage values as well as the keywords auto, contain, and cover.
`background-size: contain;`
* The background-clip property can be used to specify whether an element's background extends into the border or not. The background-clip property can take the three values: border-box, padding-box, content-box.`background-clip: content-box;`
* The background-origin property can be used to specify the positioning area of the background images. It can take the same values as background-clip property: border-box, padding-box, content-box.`background-origin: content-box;`
* CSS3 gives you ability to add multiple backgrounds to a single element. The backgrounds are layered on the top of one another. The number of layers is determined by the number of comma-separated values in the background-image or background shorthand property.`background: url("images/birds.png") no-repeat center,  url("images/clouds.png")  no-repeat center, lightblue;`

### Gradients
* The CSS3 gradient feature provides a flexible solution to generate smooth transitions between two or more colors
* To create a linear gradient you must define at least two color stops. However to create more complex gradient effects you can define more color stops

top-to-bottom: ` background: linear-gradient(red, yellow);`

Left to Right: `background: linear-gradient(to right, red, yellow);`

Diagonal: `background: linear-gradient(to top right, red, yellow);`

Setting Direction of Linear Gradients Using Angles: `background: linear-gradient(90deg, red, yellow);`

Linear Gradients Using Multiple Color Stops: `background: linear-gradient(red, yellow, lime);`

Location Color Stops: ` background: linear-gradient(red, yellow 30%, lime 60%);`

Repeating the Linear Gradients: `repeating-linear-gradient(black, white 10%, lime 20%);`

* In a radial gradient color emerge from a single point and smoothly spread outward in a circular or elliptical shape rather than fading from one color to another in a single direction as with linear gradients
* The arguments of the radial-gradient() function has the following meaning:

position — Specifies the starting point of the gradient, which can be specified in units (px, em, or percentages) or keyword (left, bottom, etc).

shape — Specifies the shape of the gradient's ending shape. It can be circle or ellipse.

size — Specifies the size of the gradient's ending shape. The default is farthest-side.
`background: radial-gradient(circle, red, yellow, lime);` `  background: radial-gradient(circle farthest-side at left bottom, red, yellow, lime);`

### TextOverflow
* Text can overflow, when it is prevented from wrapping, for example, if the value of white-space property is set to nowrap for the containing element or a single word is too long to fit like a long email address. In such situation you can use the CSS3 text-overflow property to determine how the overflowed text content will be displayed.
* Values Accepted by the word-break property are: clip and ellipsis and string
* `text-overflow: clip; /* clipped the overflowed text */`
* `text-overflow: ellipsis; /* display '…' to represent clipped text */`
* You can also break a long word and force it to wrap onto a new line that overflows the boundaries of containing element using the CSS3 word-wrap property. `word-wrap: break-word;`
* You can also specify the line breaking rules for the text (i.e. how to break lines within words) yourself using the CSS3 word-break property. alues Accepted by the word-break property are: normal, break-all and keep-all.


### Drop Shadow
* The box-shadow property can be used to add shadow to the element's boxes. You can even apply more than one shadow effects using a comma-separated list of shadows. The basic syntax of creating a box shadow can be given with:`box-shadow: offset-x offset-y blur-radius color;`
* offset-x — Sets the horizontal offset of the shadow.
offset-y — Sets the vertical offset of the shadow.
blur-radius — Sets the blur radius. The larger the value, the bigger the blur and more the shadow's edge will be blurred. Negative values are not allowed.
color — Sets the color of the shadow. If the color value is omitted or not specified, it takes the value of the color property.
* ` box-shadow: 5px 5px 10px #999;`
* You can use the text-shadow property to apply the shadow effects on text. You can also apply multiple shadows to text using the same notation as box-shadow. ` text-shadow: 5px 5px 10px #666;`


### Multi column layout
* The CSS3 has introduced the multi-column layout module for creating multiple column layouts in an easy and efficient way. Now you can create layouts like you see in magazines and newspapers without using the floating boxes. Here is a simple example of splitting some text into three columns using the CSS3 multiple column layout feature.`column-count: 3; /* Standard syntax */`
* The CSS properties column-count and column-width control whether and how many columns will appear. The column-count property sets the number of columns inside the multicol element, whereas the column-width property sets the desired width of the columns. `column-width: 150px; /* Standard syntax */`
* You can control the gap between columns using the column-gap property. The same gap is applied between each column. The default gap is normal which is equivalent to 1em. `column-gap: 100px;`
* You can also add a line between the columns i.e. the rule using the column-rule property. It is a shorthand property for setting width, style, and color of the rule in a single declaration. The column-rule property takes the same values as border and outline.`column-rule: 2px solid red;`


### Box sizing
* By default, the actual width or height of an element's box visible/rendered on a web page depends on its width or height, padding and border property. For example, if you apply some padding and border on a <div> element with 100% width the horizontal scrollbar will appear,he box-sizing property alter the default CSS box model in such a way that, any padding or border specified on the element is laid out and drawn inside of the content area, so that the rendered width and height of the element is equal to the specified CSS width and height

  
### Flex box
* Flexbox consists of flex containers and flex items. A flex container can be created by setting the display property of an element to either flex (generate block-level flex container) or inline-flex (generate an inline flex container similar to inline-block). All child elements of flex container automatically become flex items and are laid out using the flex layout model. The float, clear, and vertical-align properties have no effect on flex items.
* Flex items are positioned inside a flex container along a flex line controlled by the flex-direction property.
* The most important aspect of the flex layout is the ability of flex items to alter their width or height to fill the available space. This is achieved with the flex property. It is shorthand property for flex-grow, flex-shrink and flex-basis properties.
* Align Flex Items along Main Axis: Flex items can be aligned along the main axis (i.e. in the horizontal direction) of the flex container using the justify-content property.flex-start — Default value. Flex items are placed at the start of the main axis.flex-end — Flex items are placed at the end of the main axis.center — Flex items are placed at the center of the main axis with equal amounts of free space at both ends. If the leftover free-space is negative i.e. if the items overflow, then the flex items will overflow equally in both directions.space-between — Flex items are distributed evenly along the main axis, where the first item placed at the main-start edge and the last one placed at the main-end. If items overflow or there's only one item, this value is equal to flex-start.space-around — Flex items are distributed evenly with half-size spaces on either end. If they overflow or there's only one item, this value is identical to center.
* Align Flex Items along Cross Axis: Flex items can be aligned along the cross axis (i.e. in the perpendicular direction) of the flex container using the align-items or align-self property. However, where the align-items is applied to the flex container, the align-self property is applied to the individual flex items, and overrides align-items. Both properties accept the following values:flex-start — Flex items are placed at the start of the cross axis.flex-end — Flex items are placed at the end of the cross axis.center — Flex items are placed at the center of the cross axis with equal amounts of free space at both ends. If the leftover free-space is negative i.e. if the items overflow, then the flex items will overflow equally in both directions.baseline — The text baseline (or inline axis) of each flex item is aligned with the baseline of the flex item with the largest font-size.stretch — The flex item stretches to fill the current row or column unless prevented by the minimum and maximum width or height. Default value for align-items property.
* Reordering Individual Flex Items: In addition to altering the flow within a flex container, you can also change the order in which individual flex items are displayed using the order property. This property accepts positive or negative integer as value. By default, all flex items are displayed and laid out in the same order as they appear in the HTML markup as the default value of order is 0.
* Enable Wrapping of Flex Items: By default, flex containers display only a single row or column of flex items. However, you can use the flex-wrap property on the flex container to control whether its flex items will wrap into multiple lines or not, if there is not sufficient space for them on one flex line.

The flex-wrap property accept the following values:

nowrap — Default value. The flex items are placed in a single line. It may cause overflow, if there is not enough space on the flex line.
wrap — The flex container breaks its flex items across multiple lines, similar to how text is broken onto a new line when it is too wide to fit on the current line.
wrap-reverse — The flex items will wrap, if necessary, but in reverse order i.e. the cross-start and cross-end directions are swapped.
 

