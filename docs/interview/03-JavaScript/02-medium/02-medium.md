### JavaScript Medium

<details>
<summary>What is Object destructuring in Javascript?</summary>

Object destructuring is the special feature in JavaScript. It is a convenient way to extract data from JavaScript objects and assign them to the variable in more readable way.

Object destructuring allows you to write less code and make it more readable, especially when working with objects with many properties.

Object destructuring provides shorthand syntax to extracting value from the objects and array.

**Syntax :**

```js
const {} = objectName;
```

**Example :**

```js showLineNumbers=true
const student = {
  name: "Yogita",
  age: "21",
  city: "Pune",
};

// Without destructuring

const name = student.name;
const age = student.age;
const city = student.city;

// With destructuring

const { name, age, city } = student;

console.log(name); // Output: Yogita
console.log(age); // Output: 21
console.log(city); // Output: Pune
```

In the above example, we created an object `student` with properties name, age, and city. Then, we used object destructuring to create variables `name`, `age`, and `city` and assigned them the corresponding values from the `student` object.

</details>

<details>
  <summary>What is Ternary Operator ?</summary>

- Ternary Operator is also called **Conditional Operator**.
- It is Used to Check the condition and execute a same part of the code based on the condition.
- Ternary Operator Includes `?` and `:`
- It has 3 parts 1st is Condition , 2nd is true part and 3rd is false part.
- In Ternary Operator ,if the condition is **true** then `2nd part will be  executed` and if the condition is **false** then `3rd part will be  executed`.

**Syntax**:

```js

condition ? value if true : value if false

```

```js showLineNumbers=true
<!DOCTYPE html>
<html>

<body>
 <script>
   let age = 60
    let result = (age > 59) ?"Senior Citizen" : "Not a Senior Citizen";
    console.log(result);
 </script>
</body>
</html>
```

**Output**:

> Senior Citizen

</details>

<details>
  <summary>Difference between Pre-Increment Operator and Post-Increment Operator?</summary>

**Pre-Increment Operator**: A Variable is **prefix(++variable)** with increment operator is called Pre-Increment Operator.

In Pre-Increment Operator it `increase the value of variable by 1 first` and then use it .

```html showLineNumbers=true
<!DOCTYPE html>
<html>
  <head>
    <title>Pre-Increment Operator</title>
    <script>
      let a = 25;
      let result = ++a;
      console.log(result);
      console.log(a);
    </script>
  </head>
</html>
```

**Output**:

> 26<br/>
> 26

**Post-Increment Operator**: A Variable is **suffix(variable++)** with increment operator is called Post-Increment Operator.

In Post-Increment Operator it `uses the current variable value` first and then it increase the value of variable by 1 first .

```html showLineNumbers=true
<!DOCTYPE html>
<html>
  <head>
    <title>Post-Increment Operator</title>
    <script>
      let a = 25;
      let result = a++;
      console.log(result);
      console.log(a);
    </script>
  </head>
</html>
```

**Output**:

> 25<br/>
> 26

<summary>Difference between let, const and var?</summary>

Firstly we will look about the difference between **let**, **const**. **let** & **const** both keywords are used to declare a variable.

**const**: So when we declare variable using const keyword let's say `const a;` so at that time of decleration and initialization is compulsary. `const a = 20;` later we can not change the value of const declare variable.

**let**: On the other hand when we declare variable using let keyword, we can declare it first, then later we can assign the value. We can do both things at the same time declaring and assigning & we can change the value of variable that are declare using let keyword.

**var**: So var is completly different as compare to this two keyword `let` & `const`, & it is not recommended to use var keyword the reason is we can redeclared it and reinitialized. So var is similar to let assigning multiple values is allowed but dangerous characteristic is we redeclare the variables which ar created using **var** keyword.

</details>

<details>
  <summary>How to handle Runtime Error in javaScript?</summary>

In javaScript, we Handle a Runtime Error by using `try-catch` block.
we put a possible error throwing code in try block and if error is occured then the catch block is caught a error and handle the error .
By using `try-catch ` we can execute a code without interrupted or stoppted the application .

```js
try {
  // Possible error throwing code
} catch (error) {
  // Handle the error here
}
```

**try ()**:
In **try** block we put possible error throwing or code block were error occure in runtime .For Example,API's call . So that we can execute this block safetly it the error occure then this error catch by **catch** block.

**catch(error)**:
**catch** block receive a error object .
In error object their are multiple parameters like `error message` , `error name` , `error stack` this things available in error object. By using error message we can safely show the message of the error to the user just like error message we can use error name and error stack also.

In this way our whole execution will not be interrupted or stopped but we will handle the error safely .

````js showLiniNumbers=true
try {
  const a = 10;
  console.log(a);
  console.log(c);
} catch (e) {
  console.log(e.message);
}
console.log("Hi");

  <summary>What is Template String?</summary>
Template string is just string in Javascript. We declare template string using `(backtik)`. Now inside this template string we can inject value of variable using placeholder. And we can create placeholder using $ doller curly bracket open close and inside this placeholder we write the name of variable. So whenver We use this string along with other strings it will consider value of variable.

**Example:**

```js showLineNumbers=true
let name = "RTC";
console.log(`Hello ${name}`);
````

**Output**

> 10 <br/>
> c is not defined <br/>
> Hi
> Hello RTC

</details>

<details>
  <summary>Explain common Math functions available in JS.</summary>
  The built-in JavaScript Math functions make it simple and accurate to perform mathematical operations in your code. They manage standard tasks like calculating powers and square roots, determining the highest or lowest integer, rounding, and more. Your code becomes shorter, faster, and less prone to errors as a result.

**Examples:-**

- `toFixed()`
- `Math.ceil(x)`
- `Math.floor(x)`
- `Math.round(x)`
- `Math.pow(x,y)`
- `Math.abs(x)`
- `Math.min(x)`
- `Math.max(x)`
- `Math.sqrt(x)`

**1.`toFixed()`**:- **toFixed()** method in JavaScript is used to format a number using fixed-point notation . By choosing how many decimal places to return, you can adjust the floating-point number.

**Syntax :**

`number.toFixed(digits)`

`number` :-The number you want to format.

`digits` :-The number of decimal places to keep in the result.

**Example :**

```js
<script>
  const number = 541.6422773427; const formattedNum = number.toFixed(2);
  console.log(formattedNum);
</script>
```

**Output :**

```
541.64
```

**2.`Math.ceil(x)`**:- Math.ceil() function in JavaScript is used to round the number passed as a parameter to its nearest integer in an Upward direction of rounding i.e. towards the greater value.

**Syntax :**

`Math.ceil(x);`

**Example :**

```js
<script>
  const value = Math.ceil(7.3); console.log("Ceiling value = " + value);
</script>
```

**Output :**

```
8
```

**3.`Math.floor(x)`**:-Javascript Math.floor() method is used to round off the number passed as a parameter to its nearest integer in a Downward direction of rounding i.e. towards the lesser value.

**Syntax :**

`Math.floor(x)`

**Example :**

```js
<script>
  const value = Math.ceil(7.3); console.log("Ceiling value = " + value);
</script>
```

**Output :**

```
7
```

**4.`Math.round(x)`**:- The Javascript Math.round() method is used to round a number to its nearest integer. If the fractional part of the number is **greater than or equal to .5**, the argument is rounded to the next higher integer. If the fractional part of the number is **less than .5**, the argument is rounded to the next lower integer.

**Syntax :**

`Math.round(x)`

**Example :**

```js
<script>
  const val1 = Math.round(6.2); console.log("Round value = " + val1); const val2
  = Math.round(6.6); console.log("Round value = " + val2);
</script>
```

**Output :**

```
   Round value = 6
   Round value = 7
```

**5.`Math.pow(x,y)`**:- The Math.pow(x, y) function in JavaScript is used to raise the base x to the power of the exponent y.

**Syntax :**

`Math.pow(x,y)`

**Example :**

```js
<script>
  const value = Math.pow(5, 2); console.log("Power of value = " + value);
</script>
```

**Output :**

```
Power of value = 25
```

**6. `Math.abs(x)`**:- This function always returns the positive (+ve) value of x.

**Syntax :**
`Math.abs(x)`

**Example :**

```js
<script>
  const val1 = Math.abs(8.4); console.log("Absolute value = " + val1); const
  val2 = Math.abs(-8.4); console.log("Absolute value = " + val2);
</script>
```

**Output :**

```
Absolute value = 8.4
Absolute value = 8.4
```

**7.`Math.min(x)`**:- It returns the minimum value from the given arguments.

**Syntax :**
`Math.min(x)`

**Example :**

```js
<script>
  const value = Math.min(10, 6, 20, 21, 17); console.log("Minimum value = " +
  value);
</script>
```

**Output :**

```
Min value = 6
```

**8.`Math.max(x)`** :- It returns the maximum value from the given arguments.

**Syntax :**
`Math.max(x)`

**Example :**

```js
<script>
  const value = Math.max(10, 16, 20, 21, 17, 55, 32); console.log("Maximum value
  = " + value);
</script>
```

**Output :**

```
Max value = 55
```

**9.`Math.sqrt(x)`** :- It returns the square root of the given arguments.

**Syntax :**
`Math.sqrt(x)`

**Example :**

```js
<script>
  const value = Math.sqrt(225); console.log("Square Root = " + value);
</script>
```

**Output :**

```
 Square Root = 15
```

</details>
