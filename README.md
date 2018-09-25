Interview Questions
===================

Table of Contents
-----------------

* [Javascript](https://github.com/SyedAfrozPasha/Javascript/tree/interview#basics)
* [React.JS](https://github.com/SyedAfrozPasha/Javascript/tree/interview#reactjs)
* [Node.JS](https://github.com/SyedAfrozPasha/Javascript/tree/interview#nodejs)
* [HTML](https://github.com/SyedAfrozPasha/Javascript/tree/interview#html)
* [CSS](https://github.com/SyedAfrozPasha/Javascript/tree/interview#css)

Javascript
----------

1. What are the different ways of creating an object in javascript?
2. What is Namespaces in javascript?
3. What is Prototypes in javascript?
4. Explain `bind`, `call` and `apply` in javascript?
5. What is Event Bubbling and Event Capturing in javascript?
6. What is Closure in javascript?
7. What is `Splice` and `Slice` in javascript?
8. What is `Map`, `Filter` and `Reduce` in javascript?
9. Difference between the `setInterval` and `setTimeout` in javascript?
10. What is callback hell in javascript and How can it be avoided?
11. What is `module.export` in javascript?
12. What is the `typeof` string, object and array in javascript?
13. AJAX: What is AJAX?
14. jQuery: List the different types of jQuery selectors?

### Javascript Coding Questions:

1. Assume two variables `a` and `b` having an object with the different `firstName` values. Add another property to both the object `lastName` with the value of `Doe` in a single line of code.
  
    ```javascript

    var a = { firstName: 'John' };
    var b = { firstName: 'Jane' };

    // Solution
    a['lastName'] = b['lastName'] = 'Doe';

    ```

2. What would be the output of following code?

    ```javascript

    console.log(10 + true); // 11
    console.log(-'24' + 10); // -14
    console.log('34' + 14); // 3414

    ```

3. What would be the output of following code?

    ```javascript

    var a = 'Hello';
    var b = new String('Hello');

    console.log(a == b); // true
    console.log(a === b); // false

    ```

4. Write a program to find whether the given string in a palindrome or not (with and without built-in javascript methods).

5. Write a program to find factorial of a given number (also handle 0!).

6. Find a maximum number present in a given array using `Math.max()` built-in method in both ES5 and ES6.

    ```javascript

    var arr = [3, 4, 1, 5, 7, 6, 2];

    // ES5
    Math.max.apply(null, arr);

    // ES6
    Math.max(...arr);

    ```

React.JS
--------

1. What is React.js?
2. What is Virtual DOM in react?
3. Difference between React.js and other JS frameworks such as Angular or Vue.js?
4. What is the main advantage of using React.js when compared to the other JS frameworks such as Angular or Vue.js? or Why React.js is better than Angular or Vue.js?
5. Difference between `state` and `props` in react? or What is `state` and `props` in react?
6. What is Higher Order Components (HOC) in react?
7. How does react works internally? (Virtual DOM)
8. What are the advantages of React.js?
9. How do you create/define a component in react?
10. What is the purpose of `render()` method in react?
11. How can we pass the props to a component in react?
12. What is Pure functions/components in react?
13. What are the life cycle methods in react?
14. For calling API's, which life cycle method of React.js should we use and why?
15. What is JSX in react?
16. What is stateful and stateless component in react?
17. What do you mean by `React.Component` and `React.PureComponent` syntax in react and when are they used?
18. What is the purpose of `super()` method in react?
19. Whether `this.setState()` in react is an asynchronous call or synchronous call?
20. MVC: Explain MVC pattern?
21. Redux: What is Redux?
22. Explain any state management architecture (Flux, Redux or MobX)?

Node.JS
-------

1. How does the `process.nextTick()` works in Node.js?
2. What is Event loop in Node.js?
3. Explain any caching technologies/techniques?
4. What is Streams in Node.js?
5. How to handle API errors in Node.js?
6. Sequelize: How to use Sequelize (NPM package) for Database operation?
7. Sequelize: List some the methods in Sequelize?
8. Express.js: How to use custom module in Express.js?

HTML
----

1. List any 5 new HTML5 tags?
2. List any 5 input types in HTML5?
3. List some of the HTML5 API's?
4. Explain GeoLocation, LocalStorage and SessionStorage HTML5 API's?
5. Difference between localStorage and sessionStorage?
6. What is the maximum data (size) that we can store in localStorage?
7. Can string, number, object and array be stored in localStorage and sessionStorage?

CSS
---

1. What is specificity rule in CSS?
2. List some of the CSS selector?
3. What is flex in CSS?
4. How can we define variables in CSS?
5. What is the difference between `display:hidden` and `visibility:hidden` properties in CSS?

### CSS Coding Questions:

  1. What will be the background color of the `div`?

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

  2. Write CSS to change the font color of 3rd, 7th and 8th `li` element to `red`.

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
  
  3. Write CSS to change the background color of alternative rows of the table to grey.

      ```css
      table>tr:nth-child(2n) {
        background-color: grey;
      }
      ```