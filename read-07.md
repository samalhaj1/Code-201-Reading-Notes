# Introduction to Domain Modeling

![Domain Modeling](https://miro.medium.com/max/5000/1*UuZRQ57iPmEKsY5wsgGBLA.jpeg)

## Defining a Domain Model:

**Domain model** is a structured visual representation of interconnected concepts or real-world objects that incorporates vocabulary, key concepts, behavior, and relationships of all of its entities.

## Creating and Initializing Objects: Constructors:

A Java class defines what objects of the class know **(attributes)** and what they can do **(behaviors)**. Each class has constructors **like World()** and **Turtle(habitat)** which are used to initialize the attributes in a newly created object.

A **new object** is created with the **new** keyword followed by the class name **(new Class())**. When this code executes, it creates a new object of the specified class and calls a constructor, which has the same name as the class. For example, **new World()** creates and initializes a new object of the World class, and **new Turtle(habitat)** creates and initializes a new Turtle object in the World habitat.

// To create a new object and call a constructor write:

// ClassName variableName = new ClassName(parameters);

World habitat = new World();    // create a new World object

Turtle t = new Turtle(habitat); // create a new Turtle object

### Define a constructor and initialize properties

To define the same properties between many objects, you'll want to use a constructor function. Below is a table that summarizes a JavaScript representation of an EpicFailVideo object.

|Property	|Data|	Type|
|---------|----|------|
|epicRating|	1 to 10	|Number|
|hasAnimals|	true or false|	Boolean|

Here's an implementation of the EpicFailVideo constructor function.

var EpicFailVideo = function(epicRating, hasAnimals) {

  this.epicRating = epicRating;
  
  this.hasAnimals = hasAnimals;
  
}

var parkourFail = new EpicFailVideo(7, false);

var corgiFail = new EpicFailVideo(4, true);

console.log(parkourFail);

console.log(corgiFail);

## Overloading Constructors

There can be more than one constructor defined in a class. This is called **overloading** the constructor. There is usually a constructor that has no parameters (nothing inside the parentheses following the name of the constructor) like the **World()** constructor above. This is also called the ***no-argument constructor.*** The ***no-argument** constructor usually sets the attributes of the object to default values.

There can also be other constructors that take parameters like the **Turtle(habitat)** constructor call above. A **parameter** (also called ***actual parameter** or ***argument**) is a value that is passed into a constructor. It can be used to initialize the attribute of an object.

The World class actually has 2 constructors. One doesn’t take any parameters and one takes the world’s width and height.

![img](https://csawesome.runestone.academy/runestone/books/published/csawesome/_images/worldConstructors.png)

**Check your understanding**

1. Which of these is overloading?

A. When a constructor takes one parameter.

B. When a constructor takes more than one parameter.

C. When one constructor is defined in a class.

D. When more than one constructor is defined in a class.

2. Which of these is valid syntax for creating and initializing a World object?

A. World w = null;

B. World w = new World;

C. World w = new World();

D. World w = World();

The constructor function is defined using a function expression. In other words, the variable ***EpicFailVideo*** is declared and then assigned a function with two parameters called ***epicRating** and ***hasAnimals.***

When the function is called, the data inside these parameters are stored inside the ***this.epicRating*** and ***this.hasAnimals*** properties respectively. Storing data within properties ensures any newly created object can access that data later.

After the constructor function definition, two objects are instantiated with the new keyword and their properties are initialized by calling the ***EpicFailVideo*** constructor function. After being instantiated and initialized, these objects are stored inside the ***parkourFail*** and ***corgiFail*** variables.

## Random Numbers

### What Random Numbers Are Used For

Random numbers have been used for many thousands of years. Whether it’s flipping a coin or rolling a dice, the goal is to leave the end result up to random chance. Random number generators in a computer are similar — they’re an attempt to achieve an unpredictable, random result.

We generally group the random numbers computers generate into two types, depending on how they’re generated: **“True”** random numbers and **pseudo** random numbers.

**To generate a “true” random number,**

The computer measures some type of physical phenomenon that takes place outside of the computer. **For example,** the computer could measure the radioactive decay of an atom. According to quantum theory, there’s no way to know for sure when radioactive decay will occur, so this is essentially “pure randomness” from the universe. An attacker wouldn’t be able to predict when radioactive decay would occur, so they wouldn’t know the random value.

**/dev/random device on Linux,**  which generates random numbers, “blocks” and doesn’t return a result until it gathers enough entropy to return a truly random number.

**Pseudorandom Numbers**

Pseudorandom numbers are an alternative to “true” random numbers. A computer could use a seed value and an algorithm to generate numbers that appear to be random, but that are in fact predictable. The computer doesn’t gather any random data from the environment.

# Tables:

HTML tables allow web developers to arrange data into rows and columns.

**Define an HTML Table**

The < table > tag defines an HTML table.

Each table row is defined with a < tr > tag. Each table header is defined with a <th> tag. Each table data/cell is defined with a < td > tag.

By default, the text in < th > elements are bold and centered.

By default, the text in < td > elements are regular and left-aligned.
  



  
**What information suits tables**
  
  In literature tables often present numerical values, cumulative statistics, categorical values, and at times parallel descriptions in form of text. They can condense large amount of information to a limited space and therefore they are popular in scientific literature in many fields of study.

**Example Complex Table**
  
In the table below, color names in four languages are given, but the first row (which includes merged cells) indicates whether the language is the Romance language or the Celtic language family. This type of table might be used in a course discussing the difference between the two language families.

![img](https://developer.mozilla.org/en-US/docs/Learn/HTML/Tables/Basics/swimming-timetable.png)
  
 # Functions, Methods, and Objects
  
  **The this Keyword**
  
In a function definition, this refers to the "owner" of the function.

In the example above, this is the person object that "owns" the fullName function.

In other words, this.firstName means the firstName property of this object.

Read more about the this keyword at JS this Keyword.
  
  **JavaScript Methods**
  
JavaScript methods are actions that can be performed on objects.

A JavaScript method is a property containing a function definition.

|Property|	Value|
|--------|-------|
|firstName|	John|
|lastName	|Doe|
|age	|50|
|eyeColor|	blue|
|fullName	|function() {return this.firstName + " " + this.lastName;}|
  
**Accessing Object Methods**
  
You access an object method with the following syntax:

**objectName.methodName()**
  
You will typically describe fullName() as a method of the person object, and fullName as a property.

The fullName property will execute (as a function) when it is invoked with ().

This example accesses the fullName() method of a person object:

***Example***
  
**name = person.fullName();**
  
  **Adding a Method to an Object**
  
Adding a new method to an object is easy:

***Example***
  
person.name = function () {
  
  return this.firstName + " " + this.lastName;
};
  
**Using Built-In Methods**
  
This example uses the toUpperCase() method of the String object, to convert a text to uppercase:

let message = "Hello world!";
  
let x = message.toUpperCase();
  
The value of x, after execution of the code above will be:

HELLO WORLD!
  
***Example***
  
person.name = function () {
  
  return (this.firstName + " " + this.lastName).toUpperCase();
  
};





