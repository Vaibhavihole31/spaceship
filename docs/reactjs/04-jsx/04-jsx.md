---
title: JSX
description: "JSX"
hide_table_of_contents: true
---

When JSX was created, it was referred to as JavaScript XML `eXtensible Markup Language` . But now `JSX` is a syntax extension for JavaScript that allows developers to write **HTML-like code** in their JavaScript files. JSX syntax allows developers to write HTML-like code in their JavaScript files, making it easier to create complex user interfaces.

`JSX` is **HTML** like syntax which enables to write **JS & HTML** at one place.

`JSX` is a syntax extension for JavaScript that allows developers to write **HTML-like code** in their JavaScript files. JSX syntax allows developers to write HTML-like code in their JavaScript files, making it easier to create complex user interfaces.

`JSX` Is extension to javascript syntax where we can write `html & js ` at the same place

### How JSX Works

Think of JSX as a special type of HTML, but with some rules:

- **Every Tag Must Be Closed**: In regular HTML, you can get away with leaving some tags open, like `<img>`. In JSX, every tag must be properly closed, even self-closing ones.

- **One Parent Element**: You can't have multiple elements hanging around on their own in JSX. They need to be wrapped inside a single parent element. It's like putting your ingredients in one container before cooking.

- **Jsx fragment** Fragments `<> </>` in React act like magic boxes, neatly organizing your elements without cluttering your webpage. They're perfect for keeping things tidy and organized without any extra fuss.

* **Jsx** JSX is JavaScript's syntax extension for writing HTML-like code directly within JavaScript files,

- **JavaScript Inside Curly Braces**: The real power of JSX is that you can include JavaScript inside your HTML-like code using curly braces `{}`. It's like adding spices to your cooking!

#### A Simple Example

```js
function App() {
  return (
    <>
      <h1>Hello {5 + 5}</h1>
    </>
  );
}
```

In this code, we're creating a component called `App`. Inside the `h1` tag, we have `Hello` and `{5 + 5}` inside curly braces. It's like saying, `Hello` and then calculating `5 + 5`, which is `10`, and adding it to our message. So, we get `Hello 10` as the final result.

**JSX Important libraries**

1. react
2. react-dom
3. react-script

All this libraries must be installed

## Why do we get this error ??

<img src="/react/04/fragmenterror.png" alt="screenshot1.png" width="600px"/>

### The most crucial part to understand is the error that occurs when you don't have a parent container in JSX. This is one of the fundamental rules of JSX - all elements must have a single parent wrapper.

Solution 1:- Wrap it using jsx fragment

```js
root.render(
  <>
    <div>Content 1</div>
    <div>Content 2</div>
  </>
);
```

Solution 2:- Wrap it using div

```js


root.render(
  <div>
   <div>Content 1</div>
   <div>Content 2</div>
  <div/>
          )
```
