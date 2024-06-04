---
title: Styling React Components
description: "Styling React Components"
hide_table_of_contents: true
---

Exploring **CSS Styling** Methods in React :

1. Inline CSS
2. Document CSS
3. External CSS

```jsx title="src/index.js" showLineNumbers="true"
import ReactDOM from "react-dom/client";
const root = ReactDOM.createRoot(document.getElementById("root"));

function Greeting(props) {
  const { name, city, age } = props;
  return (
    <div
      style={{
        border: "5px double black",
        backgroundColor: "lightblue",
        borderRadius: "10px",
        padding: "10px",
        margin: "10px",
      }}
    >
      <h1 style={{ color: "tomato" }}>
        I am {name} from {city}. I am {age} years old.
      </h1>
    </div>
  );
}
root.render(
  <>
    <Greeting name="Anand" city="Nagpur" age="23" />
    <Greeting name="Vaishnavi" city="Ahmednagar" age="22" />
    <Greeting name="Suraj" city="Bhandara" age="23" />
    <Greeting name="Pinki" city="Pune" age="20" />
  </>
);
```

**Output :**

> <img src="/react/05/screenshot1.png" alt="screenshot1.png" width="600px"/>

2. **Document CSS :** Document CSS, also known as embedded CSS, involves placing CSS styles within a `<style> tag` within the `HTML document or JSX file`. These styles apply to the entire document or a specific section, making them reusable within that document.

```jsx title="src/index.js" showLineNumbers="true"
import ReactDOM from "react-dom/client";
const root = ReactDOM.createRoot(document.getElementById("root"));

const cardStyle = {
  border: "4px double black",
  backgroundColor: "aqua",
  borderRadius: "10px",
  padding: "10px",
  margin: "10px",
};

const headingStyle = {
  color: "tomato",
};

function Greeting(props) {
  const { name, city, age } = props;
  return (
    <div style={cardStyle}>
      <h1 style={headingStyle}>
        I am {name} from {city}. I am {age} years old.
      </h1>
    </div>
  );
}
root.render(
  <>
    <Greeting name="Anand" city="Nagpur" age="23" />
    <Greeting name="Vaishnavi" city="Ahmednagar" age="22" />
    <Greeting name="Suraj" city="Bhandara" age="23" />
    <Greeting name="Pinki" city="Pune" age="20" />
  </>
);
```

`Note : in HTML we use class to take class but in react we have to use ClassName for that otherwise it will give warning.`

1. **Inline CSS :** In React, `inline CSS` refers to adding CSS styles directly to individual `JSX elements using the style attribut`e. It allows for unique and immediate styling of specific elements within a component.

**Output :**

> <img src="/react/05/screenshot2.png" alt="screenshot2.png" width="600px"/>

3. **External CSS :** External CSS refers to placing CSS styles in a separate `external file (typically with a .css extension)` and linking it to your React components. This method promotes reusability and separation of concerns, as the styles can be shared across multiple components or pages.

```jsx title="src/index.js" showLineNumbers="true"
import ReactDOM from "react-dom/client";
import "./index.css";
const root = ReactDOM.createRoot(document.getElementById("root"));

function Greeting(props) {
  const { name, city, age } = props;
  return (
    <div className="card">
      <h1>
        I am {name} from {city}. I am {age} years old.
      </h1>
    </div>
  );
}
root.render(
  <>
    <Greeting name="Anand" city="Nagpur" age="23" />
    <Greeting name="Vaishnavi" city="Ahmednagar" age="22" />
    <Greeting name="Suraj" city="Bhandara" age="23" />
    <Greeting name="Pinki" city="Pune" age="20" />
  </>
);
```

**File Name : index.css**

```css
.card {
  border: 5px double black;
  border-radius: 10px;
  padding: 10px;
  margin: 10px;
  background-color: aquamarine;
}
```

**Output :**

> <img src="/react/05/screenshot3.png" alt="screenshot3.png" width="600px"/>

**Example :for conditions**

```jsx title="src/index.js" showLineNumbers="true"
import ReactDOM from 'react-dom/client';
import './index.css';
const root =ReactDOM.createRoot(document.getElementById("root"))

function StudentCard({name,city,gender}){
  return(
    <div className={student-card ${gender == "female" ? "bg-female" : "bg-male"}}>
      <h3 className='card-heading'>Hi I am {name} {gender}</h3>
      <p className='card-subheading'>I am from {city}</p>
    </div>
  )
}
root.render(
  <div className='student-card-container'>
    <StudentCard name="Sakshi" city="Ahmednagar" gender="female"/>
    <StudentCard name="Sneha" city="Pune" gender="female"/>
    <StudentCard name="Neha" city="Ahmednagar" gender="female"/>
    <StudentCard name="Ashish" city="Ahmednagar" gender="male"/>
    <StudentCard name="Harshal" city="Pune" gender="male"/>
    <StudentCard name="Omkar" city="Ahmednagar" gender="male"/>
 </div>

)

```

**File Name : index.css**

```css
.student-card-container {
  display: flex;
}

.student-card {
  padding-left: 20px;
  border-radius: 5px;
  margin: 10px;
  height: 200px;
  width: 200px;
}

.bg-female {
  background-color: rgb(231, 7, 26);
}

.bg-male {
  background-color: aquamarine;
}
```

**Output :**

<img src="Screenshot condition.png" alt="screenshot FOR CONDITION.png" width="600px"/>

**Explanation :**

`This code demonstrates how to create and render a React component (StudentCard) multiple times with different props, and how to conditionally apply CSS classes based on prop values.`

In line 1 and 2 ,code imports the ReactDOM module from 'react-dom/client' and an external CSS file './index.css'.

In Line 3 ,it creates a root React element using ReactDOM.createRoot(). It specifies that the root element in the HTML document with the id "root" will be the container for rendering React elements.

In line 5 to 11 , it defines a functional React component StudentCard. It takes three props: name, city, and gender. Inside the component, it returns JSX, which represents the structure and content of the component.` The class name of the <div> element is conditionally set based on the gender prop.`

In line 12 to 21 , it renders the root React element created earlier. Inside the root element, it renders a <div /> with the class name 'student-card-container', containing multiple StudentCard components with different props (name, city, gender).
