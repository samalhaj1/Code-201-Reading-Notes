# Error Handling and Debugging:

![img](https://0701.static.prezi.com/preview/v2/h3j5rflrkheepc5js3m7tae7e76jc3sachvcdoaizecfr3dnitcq_1_0.png)

## Understanding Order Execution:

![img](https://i.stack.imgur.com/OovG7.png)
**Key Takeaways:**

* Order execution is the process of accepting and completing a buy or sell order in the market on behalf of a client.

* Order execution may be carried out manually or electronically, subject to the limits or conditions placed on the order by the account holder.

* Brokers are beholden to best execution practices that are regulated by the SEC as well as individual exchanges.

## Execution context

**Execution context (EC)** is defined as the environment in which the JavaScript code is executed. By environment, I mean the value of this, variables, objects, and functions JavaScript code has access to at a particular time.

***Execution context in JavaScript is of three types as:***

**Global execution context (GEC):**

This is the default execution context in which JS code start its execution when the file first loads in the browser. All of the global code i.e. code which is not inside any function or object is executed inside the global execution context. GEC cannot be more than one because only one global environment is possible for JS code execution as the JS engine is single threaded.

**Functional execution context (FEC):**

Functional execution context is defined as the context created by the JS engine whenever it finds any function call. Each function has its own execution context. It can be more than one. Functional execution context has access to all the code of the global execution context though vice versa is not applicable. While executing the global execution context code, if JS engine finds a function call, it creates a new functional execution context for that function. In the browser context, if the code is executing in strict mode value of this is undefined else it is window object in the function execution context.

**Eval: Execution context inside eval function.**

Execution context stack (ECS): Execution context stack is a stack data structure, i.e. last in first out data structure, to store all the execution stacks created during the life cycle of the script. Global execution context is present by default in execution context stack and it is at the bottom of the stack. While executing the global execution context code, if JS engines find a function call, it creates a functional execution context for that function and pushes it on top of the execution context stack. JS engine executes the function whose execution context is at the top of the execution context stack. Once all the code of the function is executed, JS engines pop out that function’s execution context and start’s executing the function which is below it.

var a = 10;

function functionA() {

	console.log("Start function A");

	function functionB(){
		console.log("In function B");
	}

	functionB();

}

functionA();

console.log("GlobalContext");


![img](https://miro.medium.com/max/875/1*bDebsOuhRx9NMyvLHY2zxA.gif)

* As soon as the above code loads into the browser, JS engine pushes the global execution context in the execution context stack. When functionA is called from global execution context, JS engine pushes functionA execution context in the execution context stack and starts executing functionA.

* When functionB is called from functionA execution context, JS engine pushes functionB execution context in the execution context stack. Once all the code of functionB gets executed, JS engine pops out functionB execution context. After this, as functionA execution context is on top of the execution context stack, JS engine starts executing the remaining code of functionA.

* Once all the code from functionA gets executed, JS engine pops out functionA execution context from execution context stack and starts executing remaining code from the global execution context.

* When all the code is executed JS engine pops out the global execution context and execution of JavaScript ends.

* So far we have discussed how the JavaScript engine handles the execution context. Now, we will see how it creates the execution context.

***JavaScript engine creates the execution context in the following two stages:***

1. Creation phase

2. Execution phase

### Creation phase

![img](https://ui.dev/post-images/global-variables-in-creation-phase.png)
is the phase in which the JS engine has called a function but its execution has not started. In the creation phase, JS engine is in the compilation phase and it just scans over the function code to compile the code, it doesn’t execute any code.

In the creation phase, JS engine performs the following task:

1. **Creates the Activation object or the Variable object:** Activation object is a special object in JS which contain all the variables, function arguments and inner functions declaration information. As activation object is a special object it does not have the dunder proto property.

2. **Creates the scope chain:** Once the activation object gets created, the JS engine initializes the scope chain which is a list of all the variables objects inside which the current function exists. This also includes the variable object of the global execution context. Scope chain also contains the current function variable object.

3. **Determines the value of this:** After the scope chain, the JavaScript engine initializes the value of this.

function funA (a, b) {
  var c = 3;
  
  var d = 2;
  
  d = function() {
  
    return a - b;
  }
}


funA(3, 2);

* Just after funA is called and before code execution of funA starts, JS engine creates an executonContextObj for funA which can be represented as shown below:

executionContextObj = {

 variableObject: {}, // All the variable, arguments and inner function details of the funA
 
 scopechain: [], // List of all the scopes inside which the current function is this // Value of this }

* Activation object or variable object contains the argument object which has details about the arguments of the function.

It will have a property name for each of the variables and functions which are declared inside the current function. Activation object or the variable object in our case will be as shown below:

variableObject = {

  argumentObject : {
  
    0: a,
    
    1: b,
    
    length: 2
  },
  
  a: 3,
  
  b: 2
  
  c: undefined,
  
  d: undefined then pointer to the function defintion of d
  
}

### Execution phase:
In the execution phase, JS engines will again scan through the function to update the variable object with the values of the variables and will execute the code.

After the execution stage, the variable object will look like this:

variableObject = {
  argumentObject : {
    0: a,
    1: b,
    length: 2
  },
  a: 3,
  b: 2,
  c: 3,
  d: undefined then pointer to the function defintion of d
}

### Scope Chain
The scope chain is a list of all the variable objects of functions inside which the current function exists. Scope chain also consists of the current function execution object.

Consider the below code:

a = 1;

var b = 2;

cFunc = function(e) {
  var c = 10;
  var d = 15;
  
  console.log(c);
  console.log(a); 
  
  function dFunc() {
    var f = 5;
    console.log(f)
    console.log(c);
    console.log(a); 
  }
  
  dFunc();
}

cFunc(10);

* Here, when function **cFunc** is called from the global execution context, the scope chain of cFunc will look like this

**Scope chain of cFunc = [ cFunc variable object, Global Execution Context variable object]**

* When **dFunc** is called from cFunc, as **dFunc** is inside cFunc, dFunc’s scope chain consists of dFunc variable object, cFunc variable object and global execution context variable object.

**Scope chain of dFunc = [dFunc variable object,  cFunc variable object, Global execution context variable object]**


* When we try to access f inside **dFunc**, JS engine checks if f is available inside dFunc’s variable object. If it finds f’s value it console.log f’s value.

* When we try to access variable c inside **dFunc**, JS engine checks if c is available inside dFunc’s variable object. If the variable is not available, then it will move to cFunc variable object.

As variable c is not available inside **dFunc’s** variable object, JS engines moves to **cFunc’s** variable object. As c is available on cFunc variable object, it will console.log c’s value.

* When we try to log a’s value inside dFunc, JS engines will check if a is available inside **dFunc’s** variable object. If a is not available inside dFunc’s variable object, it will move to the next item in scope chain i.e. cFunc’s variable object. JS engines will check if cFunc’s variable object as variable a. Here, variable a is not available on cFunc’s variable object hence, it will check the next items in dFunc’s scope chain i.e. global execution context variable object. Here a is available on dFunc’s variable object and it will console a’ s value.

* Similarly, in the case of **cFunc**, JS engine will find variable a’s value from global execution object.
**cFunc** does not know that variable f exists. Hence if we try to access f from cFunc it will give an error. But, dFunc function has access c and d variable using the scope chain

* Closures can be explained using the scope chain context in JavaScript.













