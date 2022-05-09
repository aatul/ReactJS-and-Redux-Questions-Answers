# ReactJS and Redux Questions Answers

Looking forward to appear in React and Redux Interview, here are the key React and Redux Interview Questions with Answers only for you.

### Table of Contents
| Sr.No.        | Question      | 
| ------------- |-------------| 
| 1             |[How does React work? How does Virtual-DOM work in React?](https://github.com/aatul/ReactJS-and-Redux-Questions-Answers/blob/master/README.md#1-how-does-react-work-how-does-virtual-dom-work-in-react) | 
| 2             |[What is JSX?](https://github.com/aatul/ReactJS-and-Redux-Questions-Answers/blob/master/README.md#2-what-is-jsx) |
| 3             |[What is the difference between Element and Component?](https://github.com/aatul/ReactJS-and-Redux-Questions-Answers/blob/master/README.md#3-what-is-the-difference-between-element-and-component) |
| 4             |[What is React.createClass?](https://github.com/aatul/ReactJS-and-Redux-Questions-Answers/blob/master/README.md#4-what-is-reactcreateclass) |
| 5             |[Describe the key differences in React & Angular? / Angular vs React?](https://github.com/aatul/ReactJS-and-Redux-Questions-Answers/blob/master/README.md#5-describe-the-key-differences-in-react--angular--angular-vs-react) |
| 6             |[What are Redux-Observables?](https://github.com/aatul/ReactJS-and-Redux-Questions-Answers/blob/master/README.md#6-what-are-redux-observables) | 
| 7             |[What is React DOM and what is the difference between React DOM and React?](https://github.com/aatul/ReactJS-and-Redux-Questions-Answers/blob/master/README.md#7-what-is-react-dom-and-what-is-the-difference-between-react-dom-and-react) |
| 8             |[What are the differences between a Class component and Functional component?](https://github.com/aatul/ReactJS-and-Redux-Questions-Answers/blob/master/README.md#8-what-are-the-differences-between-a-class-component-and-functional-component) |
| 9             |[What is the difference between state and props?](https://github.com/aatul/ReactJS-and-Redux-Questions-Answers/blob/master/README.md#9-what-is-the-difference-between-state-and-props) |
| 10             |[What are Controlled components?](https://github.com/aatul/ReactJS-and-Redux-Questions-Answers/blob/master/README.md#10-what-are-controlled-components) |
---

### 1. How does React work? How does Virtual-DOM work in React?

React creates a virtual DOM. When state changes in a component it firstly runs a “diffing” algorithm, which identifies what has changed in the virtual DOM. The second step is reconciliation, where it updates the DOM with the results of diff. The HTML DOM is always tree-structured — which is allowed by the structure of HTML documents. The DOM trees are huge nowadays because of large apps. Since we are more and more pushed towards dynamic web apps (Single Page Applications — SPAs), we need to modify the DOM tree incessantly/constantly and a lot. And this is a real performance and development pain.

The Virtual DOM is an abstraction of the HTML DOM. It is lightweight and detached from the browser-specific implementation details. It is not invented by React but it uses it and provides it for free. ReactElements lives in the virtual DOM. They make the basic nodes here. Once we define the elements, ReactElements can be rendered into the "real" DOM. Whenever a ReactComponent is changing the state, diff algorithm in React runs and identifies what has changed. And then it updates the DOM with the results of diff. The point is - it’s done faster than it would be in the regular DOM.

The major features of React are:
*	It uses VirtualDOM instead of RealDOM considering that RealDOM manipulations are expensive.
*	Supports server-side rendering.
*	Follows Unidirectional data flow or data binding.
*	Uses reusable/composable UI components to develop the view.

**[Back to Top](https://github.com/aatul/ReactJS-and-Redux-Questions-Answers/blob/master/README.md#table-of-contents)**

---

### 2. What is JSX?

JSX is a syntax extension to JavaScript and comes with the full power of JavaScript.
*	 JSX produces React “elements”.
*	 You can embed any JavaScript expression in JSX by wrapping it in curly braces. 

After compilation, JSX expressions become regular JavaScript objects. This means that you can use JSX inside of if statements and for loops, assign it to variables, accept it as arguments, and return it from functions. Even Though React does not require JSX, it is the recommended way of describing our UI in React app.

For example, below is the syntax for a basic element in React with JSX and its equivalent without it.
```js
const element=(
  <h1 classname="greeting">
    Hello World!
  </h1>
```
Equivalent of the above using React.createElement
```js
const element= React.createElement(
  'h1',
  {"classname": "greeting"},
  'Hello World!'
);
```

**[Back to Top](https://github.com/aatul/ReactJS-and-Redux-Questions-Answers/blob/master/README.md#table-of-contents)**

---

### 3. What is the difference between Element and Component?

An Element is a plain object describing what you want to appear on the screen in terms of the DOM nodes or other components. Elements can contain other Elements in their props. Creating a React element is cheap. Once an element is created, it is never mutated.

The object representation of React Element would be as follows:
```js
const element = React.createElement(
  'div',
  {id: 'login-btn'},
  'Login'
)
```
The above React.createElement() function returns an object:
```js
{
  type: 'div',
  props: {
    children: 'Login',
    id: 'login-btn'
  }
}
```
And finally it renders to the DOM using ReactDOM.render():
```js
<div id='login-btn'>Login</div>
```
Whereas a component can be declared in several different ways. It can be a class with a render() method. Alternatively, in simple cases, it can be defined as a function. In either case, it takes props as an input, and returns a JSX tree as the output:
```js
const Button = ({ onLogin }) =>
  <div id={'login-btn'} onClick={onLogin}>Login</div>
```
Then JSX gets transpiled to a React.createElement() function tree:
```js
const Button = ({ onLogin }) => React.createElement(
  'div',
  { id: 'login-btn', onClick: onLogin },
  'Login'
)
```

**[Back to Top](https://github.com/aatul/ReactJS-and-Redux-Questions-Answers/blob/master/README.md#table-of-contents)**

---

### 4. What is React.createClass?

| HashMap        | HashTable      | 
| ------------- |-------------| 
|Methods are not synchronized|Key methods are synchronized|
|Not thread safe|Thread safe|
|Iterator is used to iterate the values|Enumerator is used to iterate the values|
|Allows one null key and multiple null values|Doesn’t allow anything that is null|
|Performance is high than HashTable|Performance is slow|

**[Back to Top](https://github.com/aatul/ReactJS-and-Redux-Questions-Answers/blob/master/README.md#table-of-contents)**

---

### 5. Describe the key differences in React & Angular? / Angular vs React?

| React Js        | Angular Js      | 
| ------------- |-------------| 
|React is a JavaScript library for building user interfaces.|Angular is a TypeScript-based, open-source front-end web application platform.|
|React uses a virtual DOM.|Angular uses the browser's DOM|
|React, is a JavaScript library as well, but recommends using JSX.|Angularis a JS framework by nature, but is built to use TypeScript.|
|React - Low Learning Curve|Angular - High Learning Curve|
|React is just more of a 'V' in the MVC.|Angular is a fully-featured MVC framework.|
|While React can be bundled with other programming libraries, Angular is a complete solution in itself. For unidirectional data flow, React needs to be augmented by Redux.|Angular uses a two-directional data flow process where it updates the Real DOM directly while React updates only the Virtual DOM and is concerned with the one-directional data flow.|
|Dynamic Applications: React will be a great choice because it uses a virtual DOM. It can quickly incorporate and "react" to the data changes made in the view by the users.|Single Page Apps: Angular will be a great solution because it can display all changes made to the content without reloading the current page.|
|React has a sibling by the name of React Native, which allows you to build a complete mobile app for either Android or iOS. Not a web app that runs on a mobile phone, but a full-fledged mobile app built with JavaScript.|With Angular you can build hybrid mobile apps, but let's be fair, a native mobile app will always outdo a hybrid mobile app.|

**[Back to Top](https://github.com/aatul/ReactJS-and-Redux-Questions-Answers/blob/master/README.md#table-of-contents)**

---

### 6. What are Redux-Observables?

Another popular solution for handling async operations is Redux-Observable. As the name already suggests Redux-Observable is built around the concept of observables and reactive streams. 

It is basically just a thin middleware wrapper around RxJS with just a few additional helper methods. Therefore you also need to add RxJS to your application if you want to use Redux-Observable.

Similar to how sagas are handled, side effects in Redux-Observable are separated from other redux code and are handled in so-called epics. An epic is basically just a function which takes a stream of actions and returns a new stream of actions. Note though, that an action already has flown through your reducers at the time it arrives in your epics.

**[Back to Top](https://github.com/aatul/ReactJS-and-Redux-Questions-Answers/blob/master/README.md#table-of-contents)**

---

### 7. What is React DOM and what is the difference between React DOM and React?

Prior to v0.14, all ReactDOM functionality was part of React. But later, React and ReactDOM were split into two different libraries.

As the name implies, ReactDOM is the glue between React and the DOM. Often, we will only use it for one single thing: mounting with ReactDOM. Another useful feature of ReactDOM is ReactDOM.findDOMNode() which we can use to gain direct access to a DOM element.

For everything else, there’s React. We use React to define and create our elements, for lifecycle hooks, etc. i.e. the guts of a React application.

**[Back to Top](https://github.com/aatul/ReactJS-and-Redux-Questions-Answers/blob/master/README.md#table-of-contents)**

---

### 8. What are the differences between a Class component and Functional component?

Class components allow us to use additional features such as local state and lifecycle hooks. Also, to enable our component to have direct access to our store and thus hold state.

When our component just receives props and renders them to the page, this is a ‘stateless component’, for which a pure function can be used. These are also called dumb components or presentational components.

From the previous question, we can say that our Booklist component is functional and is stateless.

--Code/Image here--

On the other hand, the BookListContainer component is a class component.

**[Back to Top](https://github.com/aatul/ReactJS-and-Redux-Questions-Answers/blob/master/README.md#table-of-contents)**

---

### 9. What is the difference between state and props?

**The basic difference is: State is mutable and Pros are immutable.**

The State is a data structure that starts with a default value when a Component mounts. It may be mutated across time, mostly as a result of user events.
Props (short for properties) are a Component’s configuration. Props are how components talk to each other. They are received from above component and immutable as far as the Component receiving them is concerned. A Component cannot change its props, but it is responsible for putting together the props of its child Components. Props do not have to just be data — callback functions may be passed in as props.

There is also the case that we can have default props so that props are set even if a parent component doesn’t pass props down.

 --Code/Image here--

Props and State do similar things but are used in different ways. The majority of our components will probably be stateless. Props are used to pass data from parent to child or by the component itself. They are immutable and thus will not be changed. State is used for mutable data, or data that will change. This is particularly useful for user input.

**[Back to Top](https://github.com/aatul/ReactJS-and-Redux-Questions-Answers/blob/master/README.md#table-of-contents)**

---

### 10. What are Controlled components?

In HTML, form elements such as <input>, <textarea>, and <select> typically maintain their own state and update it based on user input. When a user submits a form the values from the aforementioned elements are sent with the form. With React it works differently. The component containing the form will keep track of the value of the input in its state and will re-render the component each time the callback function e.g. onChange is fired as the state will be updated. A form element whose value is controlled by React in this way is called a "Controlled Component".
  
With a controlled component, every state mutation will have an associated handler function. This makes it straightforward to modify or validate user input.

**[Back to Top](https://github.com/aatul/ReactJS-and-Redux-Questions-Answers/blob/master/README.md#table-of-contents)**

---

Wish you all the best.
---
