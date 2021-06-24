# Images:

## How to add images to HTML pages:

1. **Upload your image**

This can be accomplished with copy an image hosting server, an image address. Select whichever works best for you.

2. **Open your HTML doc**

This is self-explanatory, just make sure it’s the HTML document for the place where you want to insert the image

3. **Copy and paste your image URL into an IMG tag**

![] (link image adress)

# Foreground Color In CSS

**CSS Colors**

Colors in **CSS** can be specified by the following methods:

* Hexadecimal colors
* Hexadecimal colors with transparency
* RGB colors
* RGBA colors
* HSL colors
* HSLA colors
* Predefined/Cross-browser color names
* With the currentcolor keyword

**Hexadecimal Colors**

A hexadecimal color is specified with: #RRGGBB, where the RR (red), GG (green) and BB (blue) hexadecimal integers specify the components of the color. All values must be between 00 and FF.

***Example***

Define different **HEX** colors:

* #p1 {background-color: #ff0000;}   /* red */
* #p2 {background-color: #00ff00;}   /* green */
* #p3 {background-color: #0000ff;}   /* blue */

Hexadecimal Colors With Transparency
A hexadecimal color is specified with: #RRGGBB. To add transparency, add two additional digits between 00 and FF.

***Example***

Define different HEX colors with transparency:

* #p1a {background-color: #ff000080;}   /* red transparency */
* #p2a {background-color: #00ff0080;}   /* green transparency */
* #p3a {background-color: #0000ff80;}   /* blue transparency */

**RGB Colors**

An RGB color value is specified with the rgb() function, which has the following syntax:

rgb(red, green, blue)

Each parameter (red, green, and blue) defines the intensity of the color and can be an integer between 0 and 255 or a percentage value (from 0% to 100%).

For example, the rgb(0,0,255) value is rendered as blue, because the blue parameter is set to its highest value (255) and the others are set to 0.

Also, the following values define equal color: rgb(0,0,255) and rgb(0%,0%,100%).

***Example***

Define different RGB colors:

* #p1 {background-color: rgb(255, 0, 0);}   /* red */
* #p2 {background-color: rgb(0, 255, 0);}   /* green */
* #p3 {background-color: rgb(0, 0, 255);}   /* blue */


**HSL Colors**

HSL stands for hue, saturation, and lightness - and represents a cylindrical-coordinate representation of colors.

An HSL color value is specified with the hsl() function, which has the following syntax:

hsl(hue, saturation, lightness)

Hue is a degree on the color wheel (from 0 to 360) - 0 (or 360) is red, 120 is green, 240 is blue. Saturation is a percentage value; 0% means a shade of gray and 100% is the full color. Lightness is also a percentage; 0% is black, 100% is white.

***Example***

Define different HSL colors:

* #p1 {background-color: hsl(120, 100%, 50%);}   /* green */
* #p2 {background-color: hsl(120, 100%, 75%);}   /* light green */
* #p3 {background-color: hsl(120, 100%, 25%);}   /* dark green */
* #p4 {background-color: hsl(120, 60%, 70%);}    /* pastel green */

**Predefined/Cross-browser Color Names**

140 color names are predefined in the HTML and CSS color specification.

For example: blue, red, coral, brown, etc:

***Example***

Define different color names:

* #p1 {background-color: blue;}
* #p2 {background-color: red;}
* #p3 {background-color: coral;}
* #p4 {background-color: brown;}

**The currentcolor Keyword**

The currentcolor keyword refers to the value of the color property of an element.

***Example***

The border color of the following <div> element will be blue, because the text color of the <div> element is blue:

* #myDIV {
  color: blue; /* Blue text color */
  border: 10px solid currentcolor; /* Blue border color */
}
  
# Background-color
  
**Definition and Usage**
  
* The background-color property sets the background color of an element.

* The background of an element is the total size of the element, including padding and border (but not the margin).

* Tip: Use a background color and a text color that makes the text easy to read.
  
**CSS Syntax**
  
background-color: color|transparent|initial|inherit;
  
**Property Values**
  
|Value|	Description	|
------|------------|
|color|	Specifies the background color. Look at CSS Color Values for a complete list of possible color values.	|
|transparent	|Specifies that the background color should be transparent. This is default|	
|initial|	Sets this property to its default value. Read about initial	|
|inherit|	Inherits this property from its parent element. Read about inherit|
  
***Example***
  
Set background colors for different elements:

body {
  background-color: #fefbd8;
}

h1 {
  background-color: #80ced6;
}

div {
  background-color: #d5f4e6;
}

span {
  background-color: #f18973;
}
  
# Text
  
## CSS Text Alignment
  

The text-align property is used to set the horizontal alignment of a text.

A text can be left or right aligned, centered, or justified.

The following example shows center aligned, and left and right aligned text (left alignment is default if text direction is left-to-right, and right alignment is default if text direction is right-to-left):

***Example***
  
h1 {
  text-align: center;
}

h2 {
  text-align: left;
}

h3 {
  text-align: right;
}
  
## Text Direction
The direction and unicode-bidi properties can be used to change the text direction of an element:

**Example**
  
p {
  direction: rtl;
  unicode-bidi: bidi-override;
}
  
  




