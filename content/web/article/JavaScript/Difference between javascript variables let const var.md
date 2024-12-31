---
title: 'JavaScript Variables: Let, Const, and Var Differences Explained'
categories:
- Web Development
tags:
- JavaScript
date: 2024-10-17T15:30:03+00:00
author: ["Balaji"]
description: "Understanding JavaScript variable declaration is crucial for writing efficient code. This article explains the difference between JavaScript variables let const var, focusing on JavaScript let vs var vs const, when to use let const var in JavaScript, JavaScript variable scope explained, JavaScript variable hoisting explained, and the const vs let JavaScript performance comparison."
keywords: ["javascript variable declaration, difference between javascript variables let const var, javascript let vs var vs const, when to use let const var in javascript, javascript variable scope explained, javascript variable hoisting explained, const vs let javascript performance"]
draft: false
# images: 
# weight: 1   #Post can be pinned/ displayed top on the list by adding a weight=<num> var to page-variables
# aliases: ["/first"]
cover:
    image: "<image path/url>" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
---

In JavaScript, you do not have to explicitly declare variable types, they can change dynamically based on their values. Hence it is called **loosely-typed language**.

```javascript
  let a = 123; // variable 'a' initialized with number

  a = "abc"; // 'a' as string

  console.log(a); // Output: abc
```

Here variable `'a'` was initally declared of type number, but when redeclared with other value of type string its type gets changed dynamically of type string.

Understanding how to declare variables using `let`, `const`, and `var` is essential for learning JavaScript.

### JavaScript Variable Declaration

Variables in JavaScript are like labeled storage boxes. We use these labels to store and retrieve data. Over the years, the way we declare these variables has evolved, making `let` and `const` the modern standards over the older `var`.

Until ES5, `var` was the primary way to declare variables, which led to issues around scope and hoisting. To address these issues, `let` and `const` were introduced with ECMAScript 2015 (ES6). 

I feel that understanding the differences between `let`, `const`, and `var` is key to writing bug-free JavaScript code. So, let us break it down in this article!


### How to Differentiate Between `let`, `const`, and `var`

I will basically break down the difference between JavaScript variables `let`, `const`, and `var` into three main factors,

1. **Scope** of variables (Block scope vs Function scope)
2. **Redeclaration and Reassignment** of variables
3. **Hoisting** 

### 1. Scope of Variables
 * `let` and `const`: Block-scoped (exists within the nearest block {}). They are also function-scoped when declared inside functions.
 * `var`: Globally scoped or function scoped -- meaning it is limited to the function it is declared in. Major drawback in using `var` is, it can escape block scopes. If the developer do not have understanding about concept of hoisting, it may lead to bugs in the code.

```javascript
  function greetJSVariable() {
      if (true) {
          var x = "I am var"; // Function scoped
          let y = "I am let"; // Block scoped
          const z = "I am const"; // Block scoped

          console.log(x); // Output: I am var
          console.log(y); // Output: I am let
          console.log(z); // Output: I am const
      }

      console.log(x); // Output: I am var
      // console.log(y); // Error: y is not defined
      // console.log(z); // Error: z is not defined
  }

  greetJSVariable();
```
Here, the code shows how `var` is function-scoped and accessible outside the if block, whereas `let` and `const` are block-scoped and not accessible outside the if block.

### 2. Redeclaration and Reassignment
 * `let`: cannot be redeclared within the same scope, but it can be reassigned.
 * `const`: cannot be redeclared or reassigned. It’s a constant, meaning once it is assigned a value, that value cannot change.
 * `var`: can be redeclared and reassigned, even within the same scope. This can lead to unexpected behaviors in code.

 ```JavaScript
  let a = 10;
  a = 20; // Reassigned successfully
  // let a = 30; // Error: 'a' has already been declared

  const b = 30;
  // b = 40; // Error: Assignment to constant variable.
  // const b = 50; // Error: 'b' has already been declared

  var c = 50;
  c = 60; // Reassigned successfully
  var c = 70; // Redeclared successfully
  console.log(c); // Output: 70
 ```

### 3. Hoisting

 * `let` and `const`: variables declared using `let` and `const` are hoisted but remain in a "Temporal Dead Zone" (TDZ) until the declaration is reached, meaning you can not use them before they are defined.
 * `var`: hoisted to the top of its scope (function or global) and initialized as undefined. This means you can use the variable before it is declared, though it might lead to confusing bugs.

```javascript
  function hoistingExample() {
      console.log(a); // Output: undefined (due to hoisting)
      var a = 10;
      console.log(a); // Output: 10

      // console.log(b); // Error: Cannot access 'b' before initialization
      let b = 20;
      console.log(b); // Output: 20
  }

  hoistingExample();
```
Here, `var` is hoisted, meaning the declaration is moved to the top of the function scope, but its initialization remains in place. With `let`, hoisting does not apply in the same manner, leading to a ReferenceError if accessed before initialization.

<aside class="note">
  <ol>
    <li>Always prefer to use <code>let</code> and <code>const</code> over <code>var</code> for variable declarations in JavaScript.</li>
    <li>Use <code>const</code> when you know the value of the variable will remain constant thorughout the program. If the value might change, then use <code>let</code>.</li>
    <li><code>const</code> clearly indicate that the variable should not change, which makes your code easy to read and maintain.</li>
  </ol>
</aside>