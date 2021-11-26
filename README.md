# My CSS Documentation

### Total Chapters are following

1. Introduction
2. Selectors & Combinators
3. Typography
4. Box Model
5. Layout Design
6. How to desgin
7. Animation
8. Responsive Web Design
9. Project

<br />

## Chapter 1: Introduction

### [1.1 Introduction to CSS](https://youtu.be/_5TU7eXKeyk)

#### What is CSS & Why CSS?

- CSS stands for Cascading Style Sheets
- It is used to style **html elements**
- Initial release on December 17, 1996

### [1.2 Inline CSS](https://youtu.be/9U--RckH_IM)

- 3 main ways to add css with html: Inline CSS, Internal CSS, External CSS
- Inline CSS refers to style inside html element. Syntax: `<tagName style="property:value; property:value; ... ">`
- Inline CSS Example is given below:

  ```html
  <h1 style="background-color: green">Welcome to CSS</h1>
  <p style="color: white; background-color: green">
    aperiam fugiat blanditiis voluptatibus quo!
  </p>
  <p style="color: white; background-color: green">
    aperiam fugiat blanditiis voluptatibus quo!
  </p>
  ```

### [1.3 Internal CSS](https://youtu.be/7mQnjm8PI2w)

- Inside `<head>` tag we can use internal css with the help of `<style>` tag
- Internal CSS Syntax:

  ```html
  <style>
    selector {
      property: value;
      property: value;
      ...;
    }
  </style>
  ```

- Internal CSS Example is given below; In the example `<p>` tag is a selector:

  ```html
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <title>Learn Internal CSS</title>
      <style>
        p {
          background-color: green;
          color: white;
        }
      </>
    </head>
    <body>
      <p>Welcome to CSS</p>
      <p>aperiam fugiat blanditiis voluptatibus quo!</p>
    </body>
  </html>
  ```

### [1.4 Exetrnal CSS](https://youtu.be/f9vqFrO-iXM)

- Inside `<head>` tag we can link the external css file with the help of `<link rel="stylesheet" href="cssFileNameOrAddressHere"/> tag`
- create a css file with an extension of .css as shown below: style.css

  ```css
  p {
    background-color: green;
    color: white;
  }
  ```

- then add the css file inside html file as shown below:

  ```html
  <head>
    <title>Learn Internal CSS</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <p>Welcome to CSS</p>
    <p>aperiam fugiat blanditiis voluptatibus quo!</p>
  </body>
  ```

<br />

## Chapter 2: Selectors & Combinators

### [2.1 Basic Selectors ](https://youtu.be/T4HuTcVgcFI)

- Basic Selectors: Element Selector, grouping selectors, nested selector, Universal Selector, ID selectors, class selectors,
- Element selector: select an element by using its name.  
  Example:

  ```html
  <head>
    <style>
      h1 {
        background-color: green;
      }
    </style>
  </head>
  <body>
    <h1>Bangladesh</h1>
  </body>
  ```

- Grouping selector: select multiple element by using their names separted with comma.  
  Example:

  ```html
  <head>
    <style>
      h1,
      h2,
      p {
        background-color: green;
      }
    </style>
  </head>
  <body>
    <h1>Bangladesh</h1>
    <h2>Bangladesh</h2>
    <p>Bangladesh</p>
  </body>
  ```

- Nested selector: select elements by nesting. ul li a {...}, div p {...}
  Example:

  ```html
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <title>Learn Internal CSS</title>
      <style>
        ul li a {
          color: green;
        }
      </style>
    </head>
    <body>
      <ul>
        <li><a href="#">Google</a></li>
      </ul>
    </body>
  </html>
  ```

- Universal selector can help to select all the html elements. It is denoted by \*  
  Example:

  ```html
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <title>Learn Internal CSS</title>
      <style>
        * {
          background-color: salmon;
          color: white;
        }
      </style>
    </head>
    <body>
      <h1>Hello CSS</h1>
      <p>aperiam fugiat blanditiis voluptatibus quo!</p>
    </body>
  </html>
  ```

- id selector: is unique inside html document. #id can help to select any element with a given id. use # notation for selecting an id.
  Example:

  ```html
  <head>
    <style>
      #title {
        background-color: green;
      }
    </style>
  </head>
  <body>
    <h1 id="title">Bangladesh</h1>
  </body>
  ```

- class selector: .class can help to select any element with a given class. use dot notation for selecting a class.
  Example:

  ```html
  <head>
    <style>
      .title {
        background-color: green;
      }
    </style>
  </head>
  <body>
    <h1 class="title">Bangladesh</h1>
  </body>
  ```

### [2.2 More on Class & ID Selectors ](https://youtu.be/c3ha4Dq_tdA)

- we can use multiple class name for an html element such as `<h1 class="style1 style2" > this is something </h1>`
- selecting elements with class name, id name example is given below:

  ```html
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <title>Learn Internal CSS</title>
      <style>
        .heading h1 {
          background-color: salmon;
          color: white;
        }
        #heading2 p {
          background-color: green;
          color: white;
        }
      </style>
    </head>
    <body>
      <div class="heading">
        <h1>Hello CSS</h1>
        <p>aperiam fugiat blanditiis voluptatibus quo!</p>
      </div>
      <div id="heading2">
        <h1>Hello CSS</h1>
        <p>aperiam fugiat blanditiis voluptatibus quo!</p>
      </div>
    </body>
  </html>
  ```

### [2.3 Selectors & Combinators](https://youtu.be/tzsteHDBb9g)

- Attribute selectors

  - References: https://developer.mozilla.org/en-US/docs/Web/CSS/Attribute_selectors
  - syntax for Attribute selectors

    ```css
    /*for attribute name attr.*/
    element[attr] {
      property: value;
    }

    /*for attribute name attr with exactly same value.*/
    element[attr="value"] {
      property: value;
    }

    /* element with "value" anywhere in the url.*/
    element[attr*="value"] {
      property: value;
    }

    /* element with "value" anywhere in the url without case sensitivity.*/
    element[attr*="value" i] {
      property: value;
    }

    /* element end with .value; mainly for link(a) tag.*/
    element[attr$=".value"] {
      property: value;
    }
    ```

- Pseudo class selectors
  - Link Pseudo classes: link, visited, hover, active
  - Input Pseudo classes: focus, enabled, disabled, checked, required, optional, valid, invalid
  - General Pseudo classes: first-child, last-child, first-of-type, last-of-type, nth-child(n), nth-last-child(n), nth-last-of-type(n), root, not
  - References: https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes
  - syntax for Pseudo class selectors
    ```css
    selector:pseudo-class {
      property: value;
    }
    ```
- Pseudo element selectors
  - Common Pseudo element: after, before, first-letter, first-line, placeholder, select
  - References: https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements
  - syntax for Pseudo element selectors
    ```css
    selector::pseudo-element {
    property: value;
    }
    -- Child selectors (div > p)
    ```
- descendent selectors (div p)
- adjacent selectors (div + p)
- general sibling selectors (div ~ p)

### [2.4 CSS Specificity]()

- References:
  - https://www.w3.org/TR/selectors-3/#specificity
  - specificity calculator: https://specificity.keegan.st/
- Universal selector (\*) specificity - 0
- Count the number of Elements and Pesudo elements (c) - 1
- Count the number of Classes, attributes, Pseudo classes (b) - 10
- Count the number of IDs (a) - 100
- Inline CSS - 1000
- !important - 10000

- How to calculate specificity

  ```css
  /* specificity calculator */
  /* a=number of id  */
  /* b=number of class, pseduo classes, attributes  */
  /* b=number of elements, pesudo elemnts, attributes  */

  /* a=0 b=0 c=1 === 001 */
  h1 {
    background-color: grey;
  }

  /* a=0 b=1 c=1  === 011 */
  h1.heading {
    background-color: blue;
  }

  /* a=0 b=1 c=0  === 010 */
  .heading {
    background-color: green;
  }

  /* a=1 b=1 c=0  === 100 */
  #head {
    background-color: red;
  }

  /* a=1 b=0 c=1  === 101 */
  h1#head {
    background-color: pink;
  }

  /* a=1 b=1 c=1  === 111 */
  h1#head.heading {
    background-color: brown;
  }
  ```
