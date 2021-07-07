## 1. Introducing CSS Transformations

![image](https://storage.stfalcon.com/uploads/images/5881e0b98e717.png)

The effect of a CSS Transform is to modify the appearance of an element in the browser by translation, rotation or other means. When defined in a style sheet, transformations are applied as the page is rendered, so you don't actually see any animations taking place. Transforms can also be applied as a mouseover or similar effect which you can see in the next section.

## 2. How to Use CSS Transitions?
To create a transition effect, you must specify two things:

* the CSS property you want to add an effect to 
* the duration of the effect

**Note:** If the duration part is not specified, the transition will have no effect, because the default value is 0.

**EXAMPLE**

    div {
    width: 100px;
    height: 100px;
    background: red;
    transition: width 2s;
    }

### Specify the Speed Curve of the Transition

![image](http://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2019/09/CSS-Transition-1.png)

The transition-timing-function property specifies the speed curve of the transition effect.

The transition-timing-function property can have the following values:

* **ease** - specifies a transition effect with a slow start, then fast, then end slowly (this is default)
* **linear** - specifies a transition effect with the same speed from start to end
* **ease-in** - specifies a transition effect with a slow start
* **ease-out** - specifies a transition effect with a slow end
* **ease-in-out** - specifies a transition effect with a slow start and end
* **cubic-bezier(n,n,n,n)** - lets you define your own values in a cubic-bezier function

### Transition + Transformation
The following example adds a transition effect to the transformation:

**EXAMPLE**

    div {
    transition: width 2s, height 2s, transform 2s;
    }
    
## 3. CSS 2D Transforms

CSS transforms allow you to move, rotate, scale, and skew elements.

### CSS 2D Transforms Methods
With the CSS transform property you can use the following 2D transformation methods:

* translate()
* rotate()
* scaleX()
* scaleY()
* scale()
* skewX()
* skewY()
* skew()
* matrix()

### The translate() Method
The translate() method moves an element from its current position

**EXAMPLE**

    div {
    transform: translate(50px, 100px);
    }
    
### The rotate() Method   
The rotate() method rotates an element clockwise or counter-clockwise according to a given degree.

**EXAMPLE**

    div {
    transform: rotate(20deg);
    }
    
### The scale() Method


The scale() method increases or decreases the size of an element (according to the parameters given for the width and height).

The following example increases the <div> element to be two times of its original width, and three times of its original height: 

**EXAMPLE**
  
     div {
     transform: scale(2, 3);
     }
  
  ## 4. CSS Animations
  
 ###  What are CSS Animations?
  
  ![image](https://cssanimation.rocks/images/posts/transitions-animations/transitions-animations.png)
  
  
An animation lets an element gradually change from one style to another.

You can change as many CSS properties you want, as many times as you want.

To use CSS animation, you must first specify some keyframes for the animation.

Keyframes hold what styles the element will have at certain times.
  
**EXAMPLE**
  
  
    /* The animation code */
    @keyframes example {
    0%   {background-color:red; left:0px; top:0px;}
    25%  {background-color:yellow; left:200px; top:0px;}
    50%  {background-color:blue; left:200px; top:200px;}
    75%  {background-color:green; left:0px; top:200px;}
    100% {background-color:red; left:0px; top:0px;}
    }

    /* The element to apply the animation to */
    div {
    width: 100px;
    height: 100px;
    position: relative;
    background-color: red;
    animation-name: example;
    animation-duration: 4s;
    }
  
  
  
  













