# HTML Lists
HTML lists allow web developers to group a set of related items in lists.

**Example**

An **unordered HTML** list:

* Item
* Item
* Item
* Item

An **ordered** HTML list:

1. First item

2.  Second item

3. Third item

4. Fourth item

**Unordered HTML List**

An unordered list starts with the <ul> tag. Each list item starts with the <li> tag.

The list items will be marked with bullets (small black circles) by default:

**Example**
  
< ul >
  
< li >Coffee< / li >
  
< li >Tea< / li >
  
< li >Milk< / li >
  
< / ul >

**Ordered HTML List**
  
An ordered list starts with the <ol> tag. Each list item starts with the <li> tag.

The list items will be marked with numbers by default:

**Example**
  
< ol >
  
< li >Coffee< / li >
  
< li >Tea< / li >
  
< li >Milk< / li >
  
< / ol >
   
**HTML Description Lists**
  
HTML also supports description lists.

A description list is a list of terms, with a description of each term.

The **< dl >** tag defines the description list, the <dt> tag defines the term (name), and the <dd> tag describes each term:

**Example**
  
< dl >
  
< dt >Coffee< / dt >
  
< dd >- black hot drink< / dd >
  
< dt >Milk< / dt >
  
< dd >- white cold drink< / dd >
  
< / dl >
  
|HTML List Tags| Tag	Description|
|---------------|-----------------|
|< ul >|	Defines an unordered list|
|< ol >|	Defines an ordered list|
|< li >|	Defines a list item|
|< dl >|	Defines a description list|
|< dt >|	Defines a term in a description list|
|< dd >|	Describes the term in a description list|
  
  
* **Box dimensions**
  
Each box has a content area (e.g., text, an image, etc.) and optional surrounding padding, border, and margin areas; the size of each area is specified by properties defined below. The following diagram shows how these areas relate and the terminology used to refer to pieces of margin, border, and padding:
  
![ box model]( https://www.w3.org/TR/CSS2/images/boxdim.png)
  
* **Margin properties:** 'margin-top', 'margin-right', 'margin-bottom', 'margin-left', and 'margin'
  
* **Padding properties:** 'padding-top', 'padding-right', 'padding-bottom', 'padding-left', and 'padding'
  
* **Border properties**
  
The border properties specify the width, color, and style of the border area of a box. These properties apply to all elements.
  
* **Border color:** 'border-top-color', 'border-right-color', 'border-bottom-color', 'border-left-color', and 'border-color'
  
* **Border style:** 'border-top-style', 'border-right-style', 'border-bottom-style', 'border-left-style', and 'border-style'
  
* **Put Quotation Marks in a String**
  
In Visual Basic, insert two quotation marks in a row as an embedded quotation mark. In Visual C# and Visual C++, insert the escape sequence \" as an embedded quotation mark. For example, to create the preceding string, use the following code.
  
private void InsertQuote(){  
  
   textBox1.Text = "She said, \"You deserve a treat!\" ";  
}
  
or-

Insert the ASCII or Unicode character for a quotation mark. In Visual Basic, use the ASCII character (34). In Visual C#, use the Unicode character (\u0022).
  
private void InsertAscii(){   
  
   textBox1.Text = "She said, " + '\u0022' + "You deserve a treat!" + '\u0022';  
}
  
**Java Logical Operators**
  
Logical operators are used to determine the logic between variables or values:

|Operator|	Name	|Description|	Example|	
---------|--------|-----------|--------|
|&& 	|Logical and|	Returns true if both statements are true|	x < 5 &&  x < 10|	
| \ \ 	|Logical or|	Returns true if one of the statements is true|	x < 5 || x < 4|	
|!|Logical not	|Reverse the result, returns false if the result is true	|!(x < 5 && x < 10)|
  
** If ... Else**
  
**Java Conditions and If Statements**
  
Java supports the usual logical conditions from mathematics:

Less than:**a < b**
                
Less than or equal to: **a <= b**
  
Greater than: **a > b**
  
Greater than or equal to: **a >=** 
  
Equal to **a == b**
  
Not Equal to: **a != b**
  
You can use these conditions to perform different actions for different decisions.

Java has the following conditional statements:

Use *if* to specify a block of code to be executed, *if* a specified condition is true
  
Use *else* to specify a block of code to be executed, *if* the same condition is false
  
Use *else if* to specify a new condition to test, *if* the first condition is false
  
Use *switch* to specify many alternative blocks of code to be executed
  
Everything Without a "Value" is False
  
* The Boolean value of 0 (zero) is false:

let x = 0;
  
Boolean(x);       // returns false
  
* The Boolean value of -0 (minus zero) is false:

let x = -0;
  
Boolean(x);       // returns false
  
* The Boolean value of "" (empty string) is false:

let x = "";
  
Boolean(x);       // returns false
  
* The Boolean value of undefined is false:

let x;
  
Boolean(x);       // returns false
  
The Boolean value of null is false:

let x = null;
  
Boolean(x);       // returns false
  
* The Boolean value of false is (you guessed it) false:

let x = false;
  
Boolean(x);       // returns false
  
* The Boolean value of NaN is false:

let x = 10 / "Hallo";
  
Boolean(x);       // returns false
  
  
* When using the == operator, equal booleans are equal:

**Example**
  
let x = false;  
  
let y = new Boolean(false);

// (x == y) is true because x and y have equal values
  
* When using the === operator, equal booleans are not equal, because the === operator expects equality in both type and value.

**Example**
  
let x = false;
  
let y = new Boolean(false);

* // (x === y) is false because x and y have different types
Or even worse. Objects cannot be compared:

**Example**
  
let x = new Boolean(false);
  
let y = new Boolean(false);

* // (x == y) is false because objects cannot be compared

  

  
  
  



 
