# Forms

## HTML Form Controls

![Form Controls](https://cdn.educba.com/academy/wp-content/uploads/2019/07/HTML-Form-Controls.png.webp)

### Introduction to HTML Form Controls

HTML is the markup language for web page creation. It defines the web page structure and behaviour. HTML consists of tags and elements that help in structuring the web pages. These elements can be grouped together inside a form to collect data from a User in a User-friendly manner. However, note that HTML is a stateless protocol that means it cannot store anything, and you will lose the data on a page refresh.


**HTML Form Control and the Structure**

There are various types of form control that are defined in the HTML; these controls are responsible for accepting the User input in a specified manner. Let’s have a look at the various types of available Form Controls in HTML.

**1) Input Text Control**

Input text controls are used to collect User data as free text. On the web page, it will form a rectangle box where Users can input the data.

There are different types of input text controls that can be used in HTML forms. Let’s have a look at the different types of input text controls.

**Single line Input Text Control**

This allows the user to enter only a single line of data. A typical example of such input text controls is for entering the name, search box, city, etc..

![img](https://cdn.educba.com/academy/wp-content/uploads/2019/06/html1.png.webp)

![img](https://cdn.educba.com/academy/wp-content/uploads/2019/06/html2.png.webp)

**Multi-line Input Text Control**

This input control type allows the user to enter data of multiple lines. Typical usage of such input controls is for comments, addresses, description and so on.

![img](https://cdn.educba.com/academy/wp-content/uploads/2019/06/html3.png.webp)
![img](https://cdn.educba.com/academy/wp-content/uploads/2019/06/html4.png.webp)

**Password Input Control**

As the name suggests, this is typically used for the password field. This works in the same way as the input text field, but the text gets masked for safety purposes.

![img](https://cdn.educba.com/academy/wp-content/uploads/2019/06/html5.png.webp)
![img](https://cdn.educba.com/academy/wp-content/uploads/2019/06/html6.png.webp)

**2) Input Type Submit**

When the input type is of submitting it performs the action defined in the form action and sends the form data to the server.

**3) Input Type Radio**

Radio buttons are used when you expect Users to fill data as a Boolean value, or you expect only one input as true out of multiple options. Some common use case of radio buttons is gender determination, employee type (Regular / Temporary), etc.

![img](https://cdn.educba.com/academy/wp-content/uploads/2019/06/html9.png.webp)

**4) Input Type Checkbox**

A checkbox lets the User select whatever information is true in his case. It is a very convenient way of accepting the data when the possible input is already known.


![img](https://cdn.educba.com/academy/wp-content/uploads/2019/06/html11.png.webp)

**5) Input Type drop-down list**

The drop-down list enables the user to select one option out of multiple possible options. This is a very User-friendly way to get the detail from the User as it provides an exhaustive list of possible options that help the user to identify the option best suits him.



![img](https://cdn.educba.com/academy/wp-content/uploads/2019/06/html13.png.webp)

**6) Input Type Optgroup**

Optgroup works in a similar way as of the drop-down list; the only difference is that the optgroup lets you to group certain options under one umbrella logically. It helps the user to quickly identify the relevant option with the help of the optgroup label.

![img](https://cdn.educba.com/academy/wp-content/uploads/2019/06/html14.png.webp)


**7) Fieldset**

Fieldset is another useful tag in the Html form that lets the developer logically group certain controls under one legend; this helps the developer give the User clear instruction on what to expect in this section.

![img](https://cdn.educba.com/academy/wp-content/uploads/2019/06/html16.png.webp)

**8) HTML output Tag**

This output tag is introduced in HTML5. It let you display the output of a calculation instantly. This is quite useful when the user needs to do a calculation instantly and see the results. A typical example of such a cases is when the user wants to check the sum of all the items present in the cart.

![img](https://cdn.educba.com/academy/wp-content/uploads/2019/06/html18.png.webp)




**9) Input type Color**

It is often required in the form to just show the color instead of any text. Input type color in HTML 5 will let you do that. It shows the color which you want to display in the form. Typical scenario’s where it is being used is to show the status of a project or a phase.
![img](https://cdn.educba.com/academy/wp-content/uploads/2019/06/html20.png.webp)

**10) Input type Date**

Input type date is commonly used where the User expects a date type field as input; it could be anything like a Date of Birth, Hiring date, termination date, etc. It is introduced in HTML 5, and the date format varies a little with the change of browser.

![img](https://cdn.educba.com/academy/wp-content/uploads/2019/06/html22.png.webp)


### How Forms Work?

A user fills in a form and then presses a button to submit the information to the server.

A form may have several form controls, each gathering different information. The server needs to know which piece of inputted data corresponds with which form element.

### HTML5: Form Validation

Before submitting data to the server, it is important to ensure all required form controls are filled out, in the correct format. This is called client-side form validation, and helps ensure data submitted matches the requirements set forth in the various form controls. This article leads you through basic concepts and examples of client-side form validation.

Prerequisites:	Computer literacy, a reasonable understanding of HTML, CSS, and JavaScript.
Objective:	To understand what client-side form validation is, why it's important, and how to apply various techniques to implement it.

#### What is form validation?

Go to any popular site with a registration form, and you will notice that they provide feedback when you don't enter your data in the format they are expecting. You'll get messages such as:

"This field is required" (You can't leave this field blank).

"Please enter your phone number in the format xxx-xxxx" (A specific data format is required for it to be considered valid).

"Please enter a valid email address" (the data you entered is not in the right format).

"Your password needs to be between 8 and 30 characters long and contain one uppercase letter, one symbol, and a number." (A very specific data format is required for your data).

This is called form validation. When you enter data, the browser and/or the web server will check to see that the data is in the correct format and within the constraints set by the application. Validation done in the browser is called client-side validation, while validation done on the server is called server-side validation. In this chapter we are focusing on client-side validation.

If the information is correctly formatted, the application allows the data to be submitted to the server and (usually) saved in a database; if the information isn't correctly formatted, it gives the user an error message explaining what needs to be corrected, and lets them try again.

# EVENTS

HTML events are "things" that happen to HTML elements.

When JavaScript is used in HTML pages, JavaScript can "react" on these events.

**HTML Events**

An HTML event can be something the browser does, or something a user does.

Here are some examples of HTML events:

* An HTML web page has finished loading
* An HTML input field was changed
* An HTML button was clicked
* Often, when events happen, you may want to do something.

1. JavaScript lets you execute code when events are detected.

HTML allows event handler attributes, with JavaScript code, to be added to HTML elements.

**With single quotes:**

< element event='some JavaScript' >

**With double quotes:**

< element event="some JavaScript" >

***Example***

< button onclick="document.getElementById('demo').innerHTML = Date()">The time is?</button >

In the example above, the JavaScript code changes the content of the element with id="demo".

2. In the next example, the code changes the content of its own element (using this.innerHTML):

***Example***

< button onclick="this.innerHTML = Date()">The time is?</button 
>
3. JavaScript code is often several lines long. It is more common to see event attributes calling functions:

***Example***

< button onclick="displayDate()">The time is?</button >

### Common HTML Events

Here is a list of some common HTML events:

|Event	|Description|
|-------|-----------|
|onchange	|An HTML element has been changed|
|onclick	|The user clicks an HTML element|
|onmouseover|	The user moves the mouse over an HTML element|
|onmouseout|	The user moves the mouse away from an HTML element|
|onkeydown|	The user pushes a keyboard key|
|onload	|The browser has finished loading the page|

### What can JavaScript Do?

* Event handlers can be used to handle and verify user input, user actions, and browser actions:

* Things that should be done every time a page loads

* Things that should be done when the page is closed

* Action that should be performed when a user clicks a button

* Content that should be verified when a user inputs data
And more ...

**Many different methods can be used to let JavaScript work with events:**

* HTML event attributes can execute JavaScript code directly

* HTML event attributes can call JavaScript functions

* You can assign your own event handler functions to HTML elements

* You can prevent events from being sent or being handled
And more ...
























