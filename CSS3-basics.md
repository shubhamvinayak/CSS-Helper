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
