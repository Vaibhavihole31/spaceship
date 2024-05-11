---
title: Components and Props
description: "Components and Props"
hide_table_of_contents: true
---

## What is Components?

JavaScript functions that returns `jsx`.

In React, a component is a reusable piece of code that defines the structure and behaviour of a part of a user interface. A component is typically written as a JavaScript function or class that returns a JSX element or a tree of elements.

We write it in PascalCase.

```jsx title="src/index.js" showLineNumbers="true"
import ReactDOM from 'react-dom/client';
const root = ReactDOM.createRoot(document.getElementById('root'));

  function  Card(){
  const randomNumber = Math.random();
  return(
    <div>
      <h1>Card {randomNumber}</h1>
    </div>
  )
}
root.render(
  <>
  <Card/>
  <Card/>
  <Card/>
  <Card/>
  </>
)
```
**Output :**
><img src="/react/03/screenshot1.png" alt="screenshot1.png" width="600px"/>

**Example Explanation :**

In Line 1, imports the ReactDOM library from the `react-dom/client` module. `ReactDOM` is a part of React that allows you to render components on a web page.

Line 2, This line creates a React `root` on the HTML element with the ID `root`. In React, the `root` is the entry point where your components will be rendered into the HTML document.

Line 4 to 11, This code defines a React functional component called `Card`. This component generates a random number and displays it within an `<h1>` tag whenever it is rendered. Essentially, it's a card component with a random number as its content.

Line 12 to 19, the `root.render()` function is used to render multiple instances of the Card component. It renders four `<Card />` components inside a React fragment (`<> ... </>`).

## What is Props? 

`props` is a shorthand for `properties`. props means Passing `Parameters` to component. It refers to a mechanism for passing data from `one component to another` in a unidirectional flow. A component can receive data as props from its parent component and use it to render its content. Props are read-only, meaning that a component cannot modify the props it receives from its parent. Overall, props help to create reusable and modular components in React.


**Example 1 :**

```jsx title="src/index.js" showLineNumbers="true"
import ReactDOM from 'react-dom/client';
const root = ReactDOM.createRoot
(document.getElementById('root'));

function Greeting(props){
  return(
    <div>
      <h1>Hello Greeting</h1>
    </div>
  )
}
root.render(
  <>
  <Greeting/>
  </>
)
```
**Output :**
>Hello Greeting

**Example Explanation :**

In this example, we are using a `JavaScript library called React` to build a web application.

In Line 1, imports the ReactDOM library from the `react-dom/client` module. `ReactDOM` is a part of React that allows you to render components on a web page.

Line 2 and 3, This line creates a React `root` on the HTML element with the ID `root`. In React, the `root` is the entry point where your components will be rendered into the HTML document.

Line 5 and 11, This line define a function called `"Greeting"` that represents a part of our web page. It displays a heading saying `"Hello Greeting."`

Line 12 and 16, This line use React to render our `"Greeting"` component inside the `"root"` element. This means the `"Hello Greeting"` message will appear on the web page inside the 'root' element.


**Example 2 :**

```jsx title="src/index.js" showLineNumbers="true"
import ReactDOM from 'react-dom/client';
const root = ReactDOM.createRoot(document.getElementById('root'));

function Greeting(props){
  console.log(props)
  return(
    <div>
      <h1>Hello</h1>
      <hr/>
    </div>
  )
}
root.render(
  <>
  <Greeting name = "Anand" city = "Pune"/>
  </>
)
```
**Output :**
><img src="/react/03/screenshot2.png" alt="screenshot2.png" width="600px"/>

**Example Explanation :**

In this example, we are using a `JavaScript library called React` to build a web application.

In Line 1, imports the ReactDOM library from the `react-dom/client` module. `ReactDOM` is a part of React that allows you to render components on a web page.

Line 2, This line creates a React `root` on the HTML element with the ID `root`. In React, the `root` is the entry point where your components will be rendered into the HTML document.

Line 4 and 12, This line define a function called `"Greeting"` that represents a part of our web page. It displays a heading saying `"Hello."` Inside the `"Greeting" component`, we use` "console.log(props)"` to show the props (information) passed to it.

Line 13 and 17, This line use React to `render the "Greeting" component inside the 'root' element`. We also pass some information `like a name ("Anand") and a city ("Pune") as props` to the "Greeting" component.

**Example 3 :**

```jsx title="src/index.js"showLineNumbers="true"
import ReactDOM from 'react-dom/client';
const root = ReactDOM.createRoot(document.getElementById('root'));

function Greeting(props){
  console.log(props)
  return(
    <div>
      <h1>I am {props.name} from {props.city}.</h1>
    </div>
  )
}
root.render(
  <>
  <Greeting name = "Anand" city = "Pune"/>
  </>
)
```
**Output :**
><img src="/react/03/screenshot3.png" alt="screenshot3.png" width="600px"/>

**Example Explanation :**

In this example, we are using a `JavaScript library called React` to build a web application.

In Line 1, imports the ReactDOM library from the `react-dom/client` module. `ReactDOM` is a part of React that allows you to render components on a web page.

Line 2, This line creates a React `root` on the HTML element with the ID `root`. In React, the `root` is the entry point where your components will be rendered into the HTML document.

Line 4 and 11, This line define a function called `"Greeting"` that takes two pieces of information (props): a person's `name` and their `city`.  Inside the `"Greeting" component`, we use` "console.log(props)"` to show the props (information) passed to it.
Inside the `"Greeting"` component, we display a message using these props, like `"I am Anand from Pune."`

Line 12 and 16, This line use React to render the "Greeting" component inside the 'root' element. We provide the `name as "Anand"` and the `city as "Pune"` as props to the "Greeting" component.

So, when you load the page, you'll see a greeting message that says, `"I am Anand from Pune,"` with the name and city values you provided as props.

**Example 4 :**

```jsx title="src/index.js" showLineNumbers="true"
import ReactDOM from 'react-dom/client';
const root = ReactDOM.createRoot(document.getElementById('root'));

function Greeting(props){
  const {name, city} = props;
  return(
    <div>
      <h1>I am {name} from {city}.</h1>
      <hr/>
    </div>
  )
}
root.render(
  <>
  <Greeting name = "Anand" city = "Nagpur"/>
  <Greeting name = "Vaishnavi" city = "Ahmednagar"/>
  <Greeting name = "Suraj" city = "Bhandara"/>
  <Greeting name = "Pinki" city = "Pune"/>
  </>
)
```
**Output :**
><img src="/react/03/screenshot4.png" alt="screenshot4.png" width="600px"/>

**Example Explanation :**

In this example, we are using a `JavaScript library called React` to build a web application.

In Line 1, imports the ReactDOM library from the `react-dom/client` module. `ReactDOM` is a part of React that allows you to render components on a web page.

Line 2, This line creates a React `root` on the HTML element with the ID `root`. In React, the `root` is the entry point where your components will be rendered into the HTML document.

Line 4 and 12, This line define a function called `"Greeting"` that takes two pieces of information (props): a person's `name` and their `city`. Inside the "Greeting" component, we use these props to create a personalized message, such as `"I am Anand from Nagpur"`. 

Line 13 and 20, This line use React to render `four` instances of the `"Greeting"` component inside the `'root'` element. Each instance has `different name and city values passed as props`.

When you open the web page, you'll see four greeting messages, each with a different name and city, like `"I am Anand from Nagpur," "I am Vaishnavi from Ahmednagar,"` and so on. 

**Example 5 :**

```jsx title="src/index.js" showLineNumbers="true"
import ReactDOM from 'react-dom/client';
const root = ReactDOM.createRoot(document.getElementById('root'));

function Greeting(props){
  const {name, city, age} = props;
  return(
    <div>
      <h1>I am {name} from {city}. I am {age} years old.</h1>
      <hr/>
    </div>
  )
}
root.render(
  <>
  <Greeting name = "Anand" city = "Nagpur" age = "23"/>
  <Greeting name = "Vaishnavi" city = "Ahmednagar" age = "22"/>
  <Greeting name = "Suraj" city = "Bhandara" age = "23"/>
  <Greeting name = "Pinki" city = "Pune" age = "20"/>
  </>
)
```
**Output :**
><img src="/react/03/screenshot5.png" alt="screenshot5.png" width="600px"/>

**Example Explanation :**

In this example, we are using a `JavaScript library called React` to build a web application.

In Line 1, imports the ReactDOM library from the `react-dom/client` module. `ReactDOM` is a part of React that allows you to render components on a web page.

Line 2, This line creates a React `root` on the HTML element with the ID `root`. In React, the `root` is the entry point where your components will be rendered into the HTML document.

Line 4 and 12, This line define a function called `"Greeting"` that takes three pieces of information (props): a person's `name`, `city` and their `age`. Inside the "Greeting" component, we use these props to create a personalized message, such as `"I am Anand from Nagpur.I am 23 years old"`.

Line 13 and 20, This line use React to render `four` instances of the `"Greeting"` component inside the `'root'` element. Each instance has `different name, city and age values passed as props`.

When you open the web page, you'll see four greeting messages, each with a different name, city and age, like `"I am Anand from Nagpur.I am 23 years old", "I am Vaishnavi from Ahmednagar. I am 22 years old,"` and so on. 