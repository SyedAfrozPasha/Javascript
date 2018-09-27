Interview Questions
===================

Table of Contents
-----------------

* [Javascript](https://github.com/SyedAfrozPasha/Javascript/tree/interview#javascript)
* [React.js](https://github.com/SyedAfrozPasha/Javascript/tree/interview#reactjs)
* [Node.js](https://github.com/SyedAfrozPasha/Javascript/tree/interview#nodejs)
* [HTML](https://github.com/SyedAfrozPasha/Javascript/tree/interview#html)
* [CSS](https://github.com/SyedAfrozPasha/Javascript/tree/interview#css)

___
Javascript
----------

**1. What are the different ways of creating an object in javascript?**

  * [Ways of creating objects in javascript](https://github.com/ganqqwerty/123-Essential-JavaScript-Interview-Questions#question-28-what-are-the-ways-of-creating-objects-in-javascript-)

**2. What is Namespaces in javascript?**

  * [JavaScript Namespace](https://www.codeproject.com/Articles/829254/JavaScript-Namespace)

**3. What is Prototypes in javascript?**

  * [Prototype in javascript](http://www.tutorialsteacher.com/javascript/prototype-in-javascript)
  * [Javascript Prototype in plain detailed language](http://javascriptissexy.com/javascript-prototype-in-plain-detailed-language/)
  * [Understanding prototypes in javascript](https://yehudakatz.com/2011/08/12/understanding-prototypes-in-javascript/)

**4. Explain `bind`, `call` and `apply` in javascript?**

  * [bind - MDN Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_objects/Function/bind)
  * [call - MDN Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function/call)
  * [apply - MDN Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function/apply)
  * [How to call, apply and bind in javascript](https://www.codementor.io/niladrisekhardutta/how-to-call-apply-and-bind-in-javascript-8i1jca6jp)

**5. What is Event Bubbling and Event Capturing in javascript?**

  * [Event bubbling and Event capturing in javascript](https://medium.com/@vsvaibhav2016/event-bubbling-and-event-capturing-in-javascript-6ff38bec30e)
  * [Event bubbling and capturing](https://javascript.info/bubbling-and-capturing)

**6. What is Closure in javascript?**

  * [Closure in Javascript](https://github.com/ganqqwerty/123-Essential-JavaScript-Interview-Questions#question-4-what-is-closure-in-javascript-can-you-provide-an-example)
  * [Master the javascript interview - What is a closure?](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-a-closure-b2f0d2152b36)
  * [Closure in detail](https://javascript.info/closure)

**7. What is `splice` and `slice` in javascript?**

  * [splice - MDN Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice)
  * [slice - MDN Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice)

**8. What is `map`, `filter` and `reduce` in javascript?**

  * [Functional javascript - map, filter and reduce](https://wsvincent.com/functional-javascript-map-filter-reduce/)
  * [Javascript functional programming - map, filter and reduce](https://medium.com/jsguru/javascript-functional-programming-map-filter-and-reduce-846ff9ba492d)
  * [reduce in javascript](https://medium.freecodecamp.org/reduce-f47a7da511a9)

**9. Difference between the `setInterval` and `setTimeout` in javascript?**

  * [setTimeout and setInterval in javascript](https://javascript.info/settimeout-setinterval)

**10. What is callback hell in javascript and How can it be avoided?**

  * [Callback hell and How to avoid it](https://blog.hellojs.org/asynchronous-javascript-from-callback-hell-to-async-and-await-9b9ceb63c8e8?_sm_pdc=1&_sm_rid=K7jkMHt785MkPtS0sWHK4b96njnDs4MHnH9DD0N)

**11. What is the `typeof` string, object and array in javascript?**

  ```javascript
  // String
  let name = 'John';
  typeof name; // "string"

  // Object
  let myObj = { name: 'Jane' };
  typeof myObj; // "object"

  // Array
  let myArr = [1, 2, 3];
  typeof myArr; // "object"
  ```

**12. AJAX: What is AJAX?**

  * [AJAX - MDN Docs](https://developer.mozilla.org/en-US/docs/Web/Guide/AJAX/Getting_Started)

**13. jQuery: List the different types of jQuery selectors?**

  * [jQuery Selectors - W3School](https://www.w3schools.com/jquery/jquery_ref_selectors.asp)
  * [Selectors - jQuery Docs](https://api.jquery.com/category/selectors/)

### Javascript Coding Questions:

**1. Assume two variables `a` and `b` having an object with the different `firstName` values. Add another property to both the object `lastName` with the value of `Doe` in a single line of code.**
  
  ```javascript

  var a = { firstName: 'John' };
  var b = { firstName: 'Jane' };

  // Solution
  a['lastName'] = b['lastName'] = 'Doe';

  ```

**2. What would be the output of following code?**

  ```javascript

  console.log(10 + true); // 11
  console.log(-'24' + 10); // -14
  console.log('34' + 14); // 3414

  ```

**3. What would be the output of following code?**

  ```javascript

  var a = 'Hello';
  var b = new String('Hello');

  console.log(a == b); // true
  console.log(a === b); // false

  ```

**4. Write a program to find whether the given string in a palindrome or not (with and without built-in javascript string methods).**

  ```javascript

  // With built-in string methods
  function isPalindrome(str) {
    // remove special characters, spaces and make lowercase
    let removeChar = str.replace(/[^A-Z0-9]/ig, "").toLowerCase();

    // reverse removeChar for comparison
    let checkPalindrome = removeChar.split('').reverse().join('');

    // Check to see if str is a Palindrome
    return (removeChar === checkPalindrome);
  }

  // Without build-in string methods
  function isPalindrome(str) {
    const len = Math.floor(str.length / 2);
    for (let i = 0; i < len; i++) {
      if (str[i] !== str[str.length - i - 1]) return false;
    }
    return true;
  }

  ```

**5. Write a program to find factorial of a given number (also handle 0!).**

  ```javascript

  function findFactorial(num) {
    if (num < 0) {
      return -1;
    } else if (num === 0) {
      return 1;
    } else {
      return (num * findFactorial(num - 1));
    }
  }

  ```

**6. Find a maximum number present in a given array using `Math.max()` built-in method in both ES5 and ES6.**

  ```javascript

  var arr = [3, 4, 1, 5, 7, 6, 2];

  // ES5
  Math.max.apply(null, arr);

  // ES6
  Math.max(...arr);

  ```

___

React.js
--------

**1. What is React.js?**

  * React js is javascript based UI Library developed at Facebook, to create an interactive, stateful & reusable UI components. 
  * Its developed by Facebook in 2011.
  * It follows the component based approach which helps in building reusable UI components.
  * It is used for developing complex and interactive web and mobile UI.

**2. What is Virtual DOM in react? or How does react works internally?**

  A virtual DOM is a lightweight JavaScript object which originally is just the copy of the real DOM. It is a node tree that lists the elements, their attributes and content as Objects and their properties. React’s render function creates a node tree out of the React components. It then updates this tree in response to the mutations in the data model which is caused by various actions done by the user or by the system.

  This Virtual DOM works in three simple steps.

  1. Whenever any underlying data changes, the entire UI is re-rendered in Virtual DOM representation.
  2. Then the difference between the previous DOM representation and the new one is calculated.
  3. Once the calculations are done, the real DOM will be updated with only the things that have actually changed.

* [How virtual dom and diffing works in react](https://medium.com/@gethylgeorge/how-virtual-dom-and-diffing-works-in-react-6fc805f9f84e)

**3. Difference between React.js and other JS frameworks such as Angular or Vue.js.**

  * [Comparison between React and Angular](https://www.c-sharpcorner.com/article/comparison-between-react-and-angular/)
  * [Angular VS React VS Vue](https://medium.com/unicorn-supplies/angular-vs-react-vs-vue-a-2017-comparison-c5c52d620176)

  * **Angular** – developed by Google, angular is a typescript based JavaScript application framework. It is also known as Super-heroic JavaScript MVW Framework. It was developed with the motive to encounter the challenges of creating single page applications. There are several versions of angular such as Angular 2+, Angular 2 or ng2. Angular is the rewritten, mostly incompatible successor to AngularJS which means AngularJS is the oldest framework.

  * **React** – React was developed by Facebook in March 2013. It is a JavaScript library that is used for building user interfaces. React creates large web applications and also provides speed, scalability, and simplicity.

  * **Vue** – Launched in February 2014, Vue is the most famous and rapidly growing framework in JS field. Vue is an intuitive, fast and composable MVVM for building interactive interfaces. It is extremely adaptable and several JavaScript libraries make use of this. Vue is also a web application framework that helps in making advanced single page applications.

**4. What is the main advantage of using React.js when compared to the other JS frameworks such as Angular or Vue.js? or Why React.js is better than Angular or Vue.js?**

  Major features of React are listed below:

  * It uses the virtual DOM instead of the real DOM.
  * It uses server-side rendering.
  * It follows uni-directional data flow or data binding.

**5. Differentiate between Real DOM and Virtual DOM.**

  | Real DOM                                 | Virtual  DOM|
  | :-------------                          |:-------------|
  | 1. It updates slow.                      | 1. It updates faster.|
  | 2. Can directly update HTML.             | 2. Can’t directly update HTML.|
  | 3. Creates a new DOM if element updates. | 3. Updates the JSX if element updates.|
  | 4. DOM manipulation is very expensive.   | 4. DOM manipulation is very easy.|
  | 5. Too much of memory wastage.           | 5. No memory wastage.|

  * [Understanding reacts virtual dom vs the real dom](https://medium.com/@hidace/understanding-reacts-virtual-dom-vs-the-real-dom-68ae29039951)

**6. Difference between `state` and `props` in react? or What is `state` and `props` in react.**

  * [State and Props in React](https://medium.com/@hareeshdevarasetty/what-is-the-difference-between-state-and-props-in-react-4034c71f678a)

**7. What is Higher Order Components (HOC) in react?**

  * [HOC - React Docs](https://reactjs.org/docs/higher-order-components.html)
  * [HOC in depth](https://medium.com/@franleplant/react-higher-order-components-in-depth-cf9032ee6c3e)
  * [Understanding HOC](https://medium.freecodecamp.org/understanding-higher-order-components-6ce359d761b)

**8. What are the advantages of React.js?**

  Advantages of React.js

  * **React.js is extremely efficient:** React.js creates its own virtual DOM where your components actually live. This approach gives you enormous flexibility and amazing gain in performance. React.js also calculates what are the changes needed to be made in DOM. This process of React.js avoids expensive DOM operations and make updates in a very client manner.
* **It makes writing Javascript easier:** React.js uses a special syntax called JSX, which allows you to mix HTML with Javascript. The user can drop a bit of HTML in the render function without having to concatenate strings, this is another fantastic thing. React.js turns those bits of HTML into functions with a special JSXTransformer.
* **It gives you out-of-the-box developer tools:** When you start your journey with React.js, do not forget to install official React.js chrome extension. It makes debugging your application much easier. After you install the extension, you will have a direct look into the virtual DOM as if you were browsing a regular DOM tree in the elements panel. Isn’t it pretty amazing!
* **It’s awesome for SEO:** One of the biggest problems with other Javascript frameworks is that they do not search engine friendly. Though there have been some improvements in this area, search engines generally have trouble reading Javascript heavy applications. React.js stands out from the crowd because you can run React.js on the server, and the virtual DOM will be rendered to the browser as a regular web page.
* **UI Test Cases:** It is extremely easy to write UI test cases because the virtual DOM system implemented entirely in JS.

**9. How do you create/define a component in react?**

  React Components let you split the UI into independent, reusable pieces, and think about each piece in isolation.
  Conceptually, components are like JavaScript functions. They accept arbitrary inputs (called “props”) and return React elements describing what should appear on the screen.

  ```javascript
  class Welcome extends React.Component {
    render() {
      return <h1>Hello, {this.props.name} </h1>;
    }
  }

  const element = <Welcome name="John" />;
  ReactDOM.render(
    element,
    document.getElementById('root')
  );
  ```

**10. What is the purpose of `render()` method in react?**

  `render()` method is used to update the UI. For this, you have to create a new element and send it to `ReactDOM.render()`. React elements are immutable and once you create an element, you cannot change its attributes. Thus, elements are like a single frame and it depicts the UI at some point. `ReactDOM.render()` controls the content of the container node you pass and if there is any DOM element already present in it then it would be replaced when first called.

**11. How can we pass the props to a component in react?**

  Props are shorthand for properties.they are very similar to an argument is passed to a pure javascript function. Props of the component are passed from parent component which invokes component. During a component’s life cycle props should not change consider them as immutable. In React all props can be accessible with this.props.

  ```javascript
  import React from 'react';
  class Welcome extends React.Component {
    render() {
      return <h1>Hello {this.props.name}</h1>;
    }
  }
  ```

**12. What is Pure functions/components in react?**

  Pure components are the simplest and fastest components which can be written. They can replace any component which only has a render(). These components enhance the simplicity of the code and performance of the application.

  * [Stateless Component vs Pure Component](https://medium.com/groww-engineering/stateless-component-vs-pure-component-d2af88a1200b)

**13. What are the life cycle methods in react?**

  * [Life cycle methods - React Docs](https://reactjs.org/docs/react-component.html)

  * [React.js component lifecycle methods - A deep dive](https://hackernoon.com/reactjs-component-lifecycle-methods-a-deep-dive-38275d9d13c0)

  * [Understanding react component life-cycle](https://code.likeagirl.io/understanding-react-component-life-cycle-49bf4b8674de)

  There are three different phases of React component’s lifecycle:

  * **Initial Rendering Phase or Mounting Phase:** This is the phase when the component is about to start its life journey and make its way to the DOM.
  * **Updating Phase:** Once the component gets added to the DOM, it can potentially update and re-render only when a prop or state change occurs. That happens only in this phase.
  * **Unmounting Phase:** This is the final phase of a component’s life cycle in which the component is destroyed and removed from the DOM.

  Some of the most important lifecycle methods are:

  * **componentWillMount()** – Executed just before rendering takes place both on the client as well as server-side.
  * **componentDidMount()** – Executed on the client side only after the first render.
  * **componentWillReceiveProps()** – Invoked as soon as the props are received from the parent class and before another render is called.
  * **shouldComponentUpdate()** – Returns true or false value based on certain conditions. If you want your component to update, return true else return false. By default, it returns false.
  * **componentWillUpdate()** – Called just before rendering takes place in the DOM.
  * **componentDidUpdate()** – Called immediately after rendering takes place.
  * **componentWillUnmount()** – Called after the component is unmounted from the DOM. It is used to clear up the memory spaces.

**14. For calling API's, which life cycle method of React.js should we use and why?**

  * The API calls should be made in **componentDidMount** method always.
  * This method is executed once in a lifecycle of a component and after the first render.
  * After a component is mounted, this method would be invoked. This is the right place to load any data from endpoint or set up any subscription.
  * Calling here `setState` will trigger re-render.

**15. What is JSX in react?**

  * JSX is an XML/HTML-like syntax used by React that extends ECMAScript so that XML/HTML-like text can co-exist with JavaScript/React code. The syntax is intended to be used by preprocessors (i.e., transpilers like Babel) to transform HTML-like text found in JavaScript files into standard JavaScript objects that a JavaScript engine will parse.
  * Basically, by using JSX you can write concise HTML/XML-like structures (e.g., DOM like tree structures) in the same file as you write JavaScript code, then Babel will transform these expressions into actual JavaScript code. Unlike the past, instead of putting JavaScript into HTML, JSX allows us to put HTML into JavaScript.

**16. What is stateful and stateless component in react?**

  | Stateful Component | Stateless Component |
  | :-------------     |:-------------       |
  |1. Stores info about component’s state change in memory| 1. Calculates the internal state of the components|
  |2. Have authority to change state|2. Do not have the authority to change state|
  |3. Contains the knowledge of past, current and possible future changes in state|3. Contains no knowledge of past, current and possible future state changes|
  |4. Stateless components notify them about the requirement of the state change, then they send down the props to them.|4. They receive the props from the Stateful components and treat them as callback functions.|

  * **Stateless components** are components that don’t have any state. When something is stateless, it calculates its internal state but it never directly mutates it.

**17. What do you mean by `React.Component` and `React.PureComponent` syntax in react and when are they used?**

  * [When to use Component or PureComponent](https://codeburst.io/when-to-use-component-or-purecomponent-a60cfad01a81)

**18. What is the purpose of `super()` method in react?**

   `super()` method is used in constructor to call the parent object methods.

**19. Whether `setState()` call in react is an asynchronous or synchronous?**

  `setState()` call in react is asynchronous in nature because React may batch multiple `setState()` calls into a single update for performance.

**20. Explain Context API in react?**

  * [Context API - React Docs](https://reactjs.org/docs/context.html)

**21. What are refs in React? and When to use it.**

  In React `ref` is used to store the reference of element or component returned by the component `render()` configuration function.Refs should be avoided in most cases, however, they can be useful when we need DOM measurements or to add methods to the components.

  Refs can be used in the following cases

  * Managing focus, text selection, or media playback.
  * Triggering imperative animations.
  * Integrating with third-party DOM libraries.

**22. MVC: Explain MVC design pattern?**

  * [MVC design pattern](https://www.geeksforgeeks.org/mvc-design-pattern/)


**23. Redux: What is Redux?**

  * [Redux](https://redux.js.org)

**24. Explain any state management architecture (Flux, Redux or MobX)?**

  * [Flux](https://facebook.github.io/flux/docs/in-depth-overview.html#content)
  * [Redux](https://redux.js.org)
  * [MobX](https://mobx.js.org/getting-started.html)

___
Node.js
-------

**1. How `process.nextTick()` works in Node.js?**

  * [How process.nexttick() works in node.js](https://medium.com/@amanhimself/how-process-nexttick-works-in-node-js-cb327812e083)

**2. What is Event loop in Node.js?**

  * [Event Loop - Node.js Docs](https://nodejs.org/en/docs/guides/event-loop-timers-and-nexttick/)
  * [What you should know to really understand the Node.js Event Loop](https://medium.com/the-node-js-collection/what-you-should-know-to-really-understand-the-node-js-event-loop-and-its-metrics-c4907b19da4c)
  * [Walking Inside the Node.js Event Loop](https://medium.freecodecamp.org/walking-inside-nodejs-event-loop-85caeca391a9)

**3. Explain any caching technologies/techniques?**

  * [Simple server side cache for Express.js with Node.js](https://medium.com/the-node-js-collection/simple-server-side-cache-for-express-js-with-node-js-45ff296ca0f0)
  * [Caching like a boss in NodeJS](https://medium.com/@danielsternlicht/caching-like-a-boss-in-nodejs-9bccbbc71b9b)

**4. What is Streams in Node.js?**

  * [Node.js Streams: Everything you need to know](https://medium.freecodecamp.org/node-js-streams-everything-you-need-to-know-c9141306be93)

**5. How to handle API errors in Node.js?**

  * [Error Handling in Node.js](https://www.joyent.com/node-js/production/design/errors)
  * [Checklist: Best Practices of Node.JS Error Handling (2018)](https://goldbergyoni.com/checklist-best-practices-of-node-js-error-handling/)

**6. What is `module.export` in Node.js?**

  * [How to use module.exports in Node.js](https://stackabuse.com/how-to-use-module-exports-in-node-js/)

**7. Sequelize: How to use Sequelize (NPM package) for Database operation?**

  * [Sequelize Docs](http://docs.sequelizejs.com/)

**8. Sequelize: List some the methods in Sequelize?**

  * [Sequelize Methods](http://docs.sequelizejs.com/manual/tutorial/models-usage.html)

**9. Express.js: How to use custom module in Express.js?**

  * [Getting started with Node.js modules: require, exports, imports and beyond](https://adrianmejia.com/blog/2016/08/12/getting-started-with-node-js-modules-require-exports-imports-npm-and-beyond/)

___
HTML
----

**1. List any 5 new HTML5 tags?**

  * [HTML5 Tags](https://www.w3schools.com/Html/html5_new_elements.asp)

**2. List any 5 input types in HTML5?**

  * [Input types in HTML5](https://www.w3schools.com/Html/html5_new_elements.asp)

**3. List some of the HTML5 API's?**

  * [HTML5 API](https://robertnyman.com/html5/)

**4. Explain GeoLocation, LocalStorage and SessionStorage HTML5 API's?**

  * [geoLocation](https://www.w3schools.com/html/html5_geolocation.asp)
  * [localStorage](https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage)
  * [sessionStorage](https://developer.mozilla.org/en-US/docs/Web/API/Window/sessionStorage)

**5. Difference between localStorage and sessionStorage?**

  **LocalStorage:**

  * Stores data with no expiration date, and gets cleared only through JavaScript, or clearing the Browser cache / Locally Stored Data
  * Storage limit is the maximum amongst the three
  
  **SessionStorage:**

  * The sessionStorage object stores data only for a session, meaning that the data is stored until the browser (or tab) is closed.
  * Data is never transferred to the server.
  * Storage limit is larger than a cookie (at least 5MB).
  
  **Cookie:**

  * Stores data that has to be sent back to the server with subsequent requests. Its expiration varies based on the type and the expiration duration can be set from either server-side or client-side (normally from server-side).
  * Cookies are primarily for server-side reading (can also be read on client-side), localStorage and sessionStorage can only be read on client-side.
  * Size must be less than 4KB.
  * Cookies can be made secure by setting the httpOnly flag as true for that cookie. This prevents client-side access to that cookie

**6. What is the maximum data (size) that we can store in localStorage?**

  * It depends on the browser, different browser has different storage limit.
  * In Chrome and IE, We can store upto 10MB (10MB seperate for localStorage and sessionStorage).
  * In Firefox, We can store upto 10MB (Combining both localStorage and sessionStorage).

  Read More on this here
  [Working with quota on mobile browsers](https://www.html5rocks.com/en/tutorials/offline/quota-research/)

**7. Can string, number, object and array be stored in localStorage and sessionStorage?**

  Yes, We can store strings, number, object and array in localStorage and sessionStorage.

___
CSS
---

**1. What is specificity rule in CSS?**

  * [CSS Specificity Rule](https://www.w3schools.com/css/css_specificity.asp)

**2. List some of the CSS selector?**

  * [CSS Selectors](https://www.sitepoint.com/css-selectors/)
  * [CSS Selector Reference](https://www.w3schools.com/cssref/css_selectors.asp)

**3. What is flex in CSS?**

  * [CSS Flex](https://www.w3schools.com/cssref/css3_pr_flex.asp)
  * [The Complete CSS Flex Box Tutorial](https://medium.com/@js_tut/the-complete-css-flex-box-tutorial-d17971950bdc)

**4. How can we define variables in CSS?**

  * [CSS Variables](https://www.w3schools.com/css/css3_variables.asp)
  * [CSS Variables — No, really!](https://medium.com/dev-channel/css-variables-no-really-76f8c91bd34e)

**5. What is the difference between `display:none` and `visibility:hidden` properties in CSS?**

  * [Stack Overflow](https://stackoverflow.com/questions/133051/what-is-the-difference-between-visibilityhidden-and-displaynone)


### CSS Coding Questions:

  **1. What will be the background color of the `div`?**

  ```html
  <div id="myDiv" class="myClass">TEXT</div>
  ```
  ```css
  #myDiv {
    background-color: red;
  }

  .myClass {
    background-color: green;
  }
  ```

  **2. Write CSS to change the font color of 3rd, 7th and 8th `li` element to `red`.**

  ```html
  <ul>
    <li>TEXT1</li>
    <li>TEXT2</li>
    <li>TEXT3</li>
    <li>TEXT4</li>
    <li>TEXT5</li>
    <li>TEXT6</li>
    <li>TEXT7</li>
    <li>TEXT8</li>
    <li>TEXT9</li>
    <li>TEXT10</li>
  </ul>
  ```
  ```css
  li:nth-child(3) {
    color: red;
  }

  li:nth-child(7) {
    color: red;
  }

  li:nth-child(8) {
    color: red;
  }
  ```
  
  **3. Write CSS to change the background color of alternative rows of the table to grey.**

  ```css
  table>tr:nth-child(2n) {
    background-color: grey;
  }
  ```