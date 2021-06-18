

# Duckett HTML Book

## A web browser
 (commonly referred to as a browser or internet browser) is an application software for accessing the World Wide Web. When a user requests a web page from a particular website, the web browser retrieves the necessary content from a web server and then displays the page on the user's device.

 ## A web server
  is computer software and underlying hardware that accepts requests via HTTP, the network protocol created to distribute web pages, or its secure variant HTTPS. A user agent, commonly a web browser or web crawler, initiates communication by making a request for a specific resource using HTTP, and the server responds with the content of that resource or an error message. The server can also accept and store resources sent from the user agent if configured to do so.

  ## A screen reader
   is a form of assistive technology (AT) that renders text and image content as speech or braille output. Screen readers are essential to people who are blind, and are useful to people who are visually impaired,illiterate, or have a learning disability. Screen readers are software applications that attempt to convey what people with normal eyesight see on a display to their users via non-visual means, like text-to-speech, sound icons, or a Braille device. They do this by applying a wide variety of techniques that include, for example, interacting with dedicated accessibility APIs, using various operating system features (like inter-process communication and querying user interface properties), and employing hooking techniques.

   ## devices

   People are accessing websites on an increasing range of devices including desktop computers, laptops, tablets, and mobile phones. It is important to remember that various devices have different screen sizes and some have faster connections to the web than others

   ## how websites are created:

   All websites use HTML and CSS, but content management systems, blogging software, and e-commerce platforms often add a few more technologies into the mix.

   ### what you see
   When you are looking at a website, it is most likely that your browser will be receiving HTML and CSS from the web server that hosts the site. The web browser interprets the HTML and CSS code to create the page that you see.

   ### how is it created:
   Small websites are often written just using HTML and CSS.Larger websites — in particular those that are updated regularly and use a content management system (CMS), blogging tools, or e-commerce software — often make use of more complex technologies on the web server, but these technologies are actually used to produce HTML and CSS that is then sent to the browser. So, if your site uses these technologies, you will be able to use your new HTML and CSS knowledge to take more control over how your site looks. Small websites are often written just using HTML and CSS.Larger websites — in particular those that are updated regularly and use a content management system (CMS), blogging tools, or e-commerce software — often make use of more complex technologies on the web server, but these technologies are actually used to produce HTML and CSS that is then sent to the browser. So, if your site uses these technologies, you will be able to use your new HTML and CSS knowledge to take more control over how your site looks.

   ### HTML5 & CSS

   Since the web was first created there have been several versions of HTML and CSS — each intended to be an improvement on the previous version. At the time of writing this book, HTML5 & CSS3 were still being developed. Although they had not been finalized, many browsers were already supporting some features of these languages and a lot of people were using the latest code on their websites. I have therefore chosen to teach you these latest versions. Because HTML5 and CSS3 build on previous versions of these languages, learning these means you will also be able to understand the earlier versions of them. I have added clear notes when the code is new and also when it might not work in older browsers.

   ## How the web work:

   When you visit a website, the web server hosting that site could be anywhere in the world. In order for you to find the location of the web server, your browser will first connect to a Domain Name System (DNS) server.

   ## structre:

   ### How Pages use Structure:

   Now think about a very different type of document — an insurance form. Insurance forms often have headings for different sections, and each section contains a list of questions with areas for you to fill in details or checkboxes to tick. Again, the structure is very similar online.

   ### Structuring word documentS:
   The use of headings and subheadings in any document often reflects a hierarchy of information. For example, a document might start with a large heading, followed by an introduction or the most important information.

   ### HTML describes the Structure of Pages:

   HTML stands for HyperText Markup Language and is the basic structural element that is used to create webpages. HTML is a markup language, which means that it is used to “mark up” the content within a document, in this case a webpage, with structural and semantic information that tells a browser how to display a page. When an HTML document is loaded by a web browser, the browser uses the HTML tags that have marked up the document to render the page’s content.
   
   There are three types of code that make up a basic website page. HTML governs the structural elements, CSS styles those elements, and JavaScript enables dynamic interaction between those elements.

   ### Basic HTML Page Structure
   
   A basic HTML page is a document that typically has the file extension .html, though HTML frequently appears in the content of other file types as well. All HTML documents follow the same basic structure so that the browser that renders the file knows what to do. The basic structure on which all webpages are built looks like this:
   
    <!DOCTYPE html>

    <html>

    <head>

        <title>Page Title</title>

    </head>

    <body>

        <h1>Homepage Headline</h1>

        <p>This is a paragraph.</p>

    </body>

    </html>

### Attributes tell uS more about eLements:

Attributes provide additional information about the contents of an element. They appear on the opening tag of the element and are made up of two parts: a name and a value, separated by an equals sign.

The attribute name indicates what kind of extra information you are supplying about the element's content. It should be written in lowercase.The value is the information or setting for the attribute. It should be placed in double quotes. Different attributes can have different values.Here an attribute called lang is used to indicate the language used in this element. The value of this attribute on this page specifies it is in US English

## Body, Head & title:

**<body>**

You met the ***<body>*** element in the first example we created. Everything inside this element is shown inside the main browser window.

**<head>**

Before the ***<body>*** element you will often see a ***<head>*** element. This contains information about the page (rather than information that is shown within the main part of the browser window that is highlighted in blue on the opposite page). You will usually find a ***<title>*** element inside the ***<head>*** element.

**<title>**

The contents of the ***<title>*** element are either shown in the top of the browser, above where you usually type in the URL of the page you want to visit, or on the tab for that page (*if your browser uses tabs to allow you to view multiple pages at the same time*)













