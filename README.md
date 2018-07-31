Javascript
==========

Basic Concepts:
---------------

* **_Syntax Parser_:**
  
  A program that reads your code and determines what it does and if its grammar or syntax is valid.

* **_Lexical Environment_:**

  Where something sits physically in the code you write.  

* **_Execution Context_:**

  The wrapper to help which manage the code that is running.
  There are lots of lexical environments. Which one is currently running is managed via execution contexts.

* **_Name/Value Pair_:**

  A name which maps to a unique value. The name may be defined more than once, but only can have one value in any given context. That value may be more name/value pairs.

* **_Object_:**

  A collection of name-value pairs.

  ```javascript
  // Example of an object
  let address = {
    street: 'Main',
    number: 100,
    apartment: {
      floor: 3,
      number: 301
    }
  }
  ```

* **_Execution context (Global)_:**
  * Execution context (Global) creates two things: _Global Object ('window' is case of browsers)_ and special variable called _'this'_.
  * This is been created by javascript engine.
  * Each window/tab has its own global execution context.
  * At global level, global object (window) is equal to 'this'.
  * Execution context is created in two phases: **_Creation Phase_** and **_Execution Phase_**
  * In _Creation Phase_, Global Object, 'this', Outer environment and Hoisting are created.
  * In _Creation Phase_, Parser runs throught the code and begins to setup translations such as where we have created variables or functions and setup memory space for variables and functions. This is called '**_Hoisting_**'.
* All variables is javascript is initial set to _undefined_ by javascript engine.
* _undefined_ is a special keyword or value in javascript. Its also one of a data type in javascript. It is assigned to a variable _which is declared but not defined_ by javascript engine.
* Defining a variable with _undefined_ is a bad practice and should be avoided.

  Example:

  ```javascript

    var a;
    console.log(a);
    if (a === undefined) { // undefined is a keyword
      console.log('a is undefined!');
    } else {
      console.log('a is defined!');
    }

  ```

* In Execution Phase, code is executed line by line.

* **_Single Threaded:_**

  It means one command is executed at a time.

* **_Synchronous:_**

  One line of code is executed at a time in order.

* Javascript is a _Single Threaded_ and _Synchronous_ execution in behaviour.

* **_Invocation:_**

  Running or calling a function. In Javascript, a function is invoked using parenthesis ().

  Example:

  ```javascript
  function b() { 
  }
  
  function a() {
    b();
  }

  a();
  ```

  Steps involved in execution:
  
  1. Firstly Global Execution Context is created.
  2. In Creation Phase, Global Object('window'), 'this' and setup memory space for function.
  3. In Execution Phase, Code is executed line by line.
  4. When it reached the line `a()`, a new execution context is created and placed on the top of _Execution Stack_. Then it run that code.
  5. Now when it reaches the line `b()`, a new execution context is created and placed on top on the `a()` execution context. Then it run that code.
  6. When `b()` is executed, its popped-off the execution stack.
  7. Similarly, if `a()` is executed, its popped-off the execution stack.

* Every function creates a new execution context and placed on top of the execution stack. When function is finishes execution, its popped-off the execution stack.

* **_Variable Environment:_**

  Where the variables live and how they relate to each other in memory. Each variable live in its own execution context.

  Example:

  ```javascript

  // Each variable live in its own execution context.

  function b() {
    var myVar;
    console.log(myVar); // output: undefined
  }

  function a() {
    var myVar = 2;
    console.log(myVar); // output: 2
    b();
  }

  var myVar = 1;
  console.log(myVar); // output: 1
  a();
  console.log(myVar); // output: 1
  ```

* Every execution context has a reference to its outer environment.

* Scope chain: lexical environment top to bottom. Outer reference that any running function has.

  Example:

  ```javascript
  // Example 1:
  // Here `b()` and `a()` are lexically sitting in the global environment.
  function b() {
    console.log(myvar); // output: 1
    // Every execution context has a reference to its outer environment.
    // Here outer lexical environment refers to Global execution context.
  }

  function a() {
    var myVar = 2;
    b();
  }

  var myVar = 1;
  a();

  ```

  ```javascript
  // Example 2:
  // Here `b()` is lexically sitting in the a() lexical environment.
  // and a() is lexically sitting in the global lexical environment.
  function a() {

    function b() {
      console.log(myvar); // output: 2
      // Here outer lexical environment refers to a() execution context.
    }

    var myVar = 2;
    b();
  }

  var myVar = 1;
  a();  
  ```

* **_Scope:_**

  Where a variable is available in the code.

* In ES6, `let` is used to declare the variable. It allows the javascript engine to use block scoping, Which means scope of a given variable is only bound to a given block of code. In execution phase, variable is placed in memory however we are not allowed to use it outside its block.

* **_Asynchronous:_**

  More than one at a time. Multiple piece of code executing at the same time.

* In browser, The javascript engine talks with the Rendering Engine which is outside the javascript engine. Rendering engine prints or renders the contents on the screen. This communication between the Rendering engine and Javascript engine is _asynchrouns_ in nature. Whereas whats happening inside the javascript engine is _synchrouns_ execution.

* Javascript Engine has list/queue to manange the events called _Event Queue_. Every event is placed on this queue when its called.

* Javascript Engine looks for _Event Queue_ after every execution context is popped-off the execution stack. Then when the execution stack is empty, events are processed from the _Event Queue_. For each event a new execution context is created on the excution stack.

* Browser places every event called in _Event Queue_ asynchrously. Whereas Javascript engine execute it one by one synchrously.

* Long running functions interupts the event calls. As the execution stack is not empty, the event are not processed.
