---
title: Anchor Tag
description: "Anchor Tag"
hide_table_of_contents: true
---

The anchor tag `<a>` is used **to create hyperlinks** in HTML, allowing users to navigate from one page to another or open external resources. It is typically used within the body of an HTML document.

**Syntax**

```html
<a href="url"> Text </a>
```

**href**: This attribute specifies the URL or destination of the hyperlink.
**Text**: This is the text or content that will be displayed as the hyperlink.

**Code :**

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Home</title>
  </head>
  <body>
    <h1>This is Homepage</h1>

    <a href="https://www.roadtocode.org/"> Click here to visit Road To Code </a>
  </body>
</html>
```

**Output :**

<img src="/html/07/output-1.png" alt="output-1" width="600px"/>

**Code :**

**File Name : homepage.html**

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Home Page</title>
  </head>
  <body>
    <h1>This is Home page</h1>
    <a href="./aboutpage.html"> Click here to visit about page </a>
    <br />
    <br />
    <a href="./contactpage.html"> Click here to visit Contact page </a>
  </body>
</html>
```

**File Name : aboutpage.html**

```html
<!DOCTYPE html>
<html>
  <head>
    <title>About Page</title>
  </head>
  <body>
    <h1>This is About page</h1>
    <a href="./contactpage.html"> Click here to visit Contact page </a>
    <br />
    <br />
    <a href="./homepage.html"> Click here to visit home page </a>
  </body>
</html>
```

**File Name : contactpage.html**

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Contact Page</title>
  </head>
  <body>
    <h1>This is Contact page</h1>
    <a href="./homepage.html"> Click here to visit home page </a>
    <br />
    <br />
    <a href="./aboutpage.html"> Click here to visit about page </a>
  </body>
</html>
```

**Output homepage.html**

<img src="/html/07/output-2.png" alt="output-2" width="600px"/>

**Output aboutpage.html**

<img src="/html/07/output-3.png" alt="output-3" width="600px"/>

**Output contactpage.html**

<img src="/html/07/output-4.png" alt="output-4" width="600px"/>

### Opening Links in New Tab

Some times we want to open the link in a new tab. We can do this by using the target attribute.
We can use the target attribute with the value `_blank` to open the link in a new tab.

**Syntax**

```html
<a href="url" target="_blank"> Visit RTC </a>
```

**Code**

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Anchor Tag</title>
    <head>
  <body>
    <a href="https://www.roadtocode.org/" target="_blank">
      Click here to visit Road To Code
    </a>
  </body>
</html>
```

:::tip
Use this when we want to keep the current page open and open the link in a new tab. So that the user can easily navigate back to the current page.
:::

**Using Anchor Tag Open Mail Address :**

**Syntax**

```html
<a href="mailto: Mail"> Text </a>
```

**Code :**

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Anchor Tag</title>
  </head>

  <body>
    <a href="mailto:suraj@roadtocode.org"> Send mail to Suraj </a>
  </body>
</html>
```

**Output :**

<img src="/html/07/output-5.png" alt="output-5" width="600px"/>
<img src="/html/07/output-6.png" alt="output-6" width="600px"/>

**Add a Clickable Telephone using Anchor Tag :**

**Syntax**

```html
<a href="tel: Number"> Text </a>
```

**Code :**

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Anchor Tag</title>
  </head>

  <body>
    <a href="tel:+918805803087"> click here to call us </a>
  </body>
</html>
```

**Output :**

<img src="/html/07/output-7.png" alt="output-7" width="600px"/>

:::info
Later, we will learn how to remove the default blue link color displayed due to the anchor tag in CSS using text-decoration.
:::
