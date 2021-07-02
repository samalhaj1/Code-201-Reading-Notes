# Images in Css

![img](https://cdn.mos.cms.futurecdn.net/Vp9WvV7YKdH4k8sKRePcE8-320-80.jpg)

## Controlling size of images in CSS

** Sometimes, it is required to fit an image into a certain given dimension. We can resize the image by specifying the width and height of an image. A common solution is to use the max-width: 100%; and height: auto; so that large images do not exceed the width of their container. The max-width and max-height properties of CSS works better, but they are not supported in many browsers.

** Another way of resizing the image is by using the object-fit property, which fits the image. This CSS property specifies how a video or an image is resized to fit its content box. It defines how an element fits into the container with an established width and height.

** The object-fit property is generally applied to image or video. This property defines how an element responds to the width and height of its container. Mainly there are five values of object-fit property such as fill, contain, cover, none, scale-down, initial, and inherit. The default value of this property is "fill".

***EXAMPLE**

![img](https://www.codegrepper.com/codeimages/changing-image-size-in-css.png)

## Aligning images in CSS

** Images are an important part of any web application. Including a lot of images in a web application is generally not recommended, but it is important to use the images wherever they required. CSS helps us to control the display of images in web applications.

** Aligning an image means to position the image at center, left and right. We can use the float property and text-align property for the alignment of images.

** If the image is in the div element, then we can use the text-align property for aligning the image in the div.

**EXAMPLE**

![img](https://www.poftut.com/wp-content/uploads/2020/03/image-121.png)

**Using float property**

The CSS float property is a positioning property. It is used to push an element to the left or right, allowing other elements to wrap around it. It is generally used with images and layouts.

Elements are floated only horizontally. So it is possible only to float elements left or right, not up or down. A floated element may be moved as far to the left or the right as possible. Simply, it means that a floated element can display at the extreme left or extreme right.

![img](https://static.javatpoint.com/csspages/images/how-to-align-images-in-css2.png)

## Adding background images

![img](https://image.slidesharecdn.com/images-1208297149858496-9/95/css-adding-background-images-2-728.jpg?cb=1208271944)

### Definition and Usage

The background-image property sets one or more background images for an element.

By default, a background-image is placed at the top-left corner of an element, and repeated both vertically and horizontally.

Tip: The background of an element is the total size of the element, including padding and border (but not the margin).

Tip: Always set a background-color to be used if the image is unavailable.

**CSS Syntax**

background-image: url|none|initial|inherit;


|Property Values| Value	Description|
|---------------|------------------|
|url('URL')|	The URL to the image. To specify more than one image, separate the URLs with a comma|
|none|	No background image will be displayed. This is default|
|linear-gradient()|	Sets a linear gradient as the background image. Define at least two colors (top to bottom)|
|radial-gradient()|	Sets a radial gradient as the background image. Define at least two colors (center to edges)|
|repeating-linear-gradient()|Repeats a linear gradient|
|repeating-radial-gradient()|	Repeats a radial gradient|
|initial	|Sets this property to its default value. Read about initial|
|inherit|	Inherits this property from its parent element. Read about inherit|
















































