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

<br />

## Chapter 3: Typography

### [3.1 Font Properties](https://youtu.be/uK7HfuCuQqo)

- `font-size: value;` here value can be px/em/rem. 1rem=16px=100%
- `font-weight: value;` here value can be 100/thin, 200/extra light, 300/light, 400/normal, 500/medium, 600/semi-medium, 700/bold, 800/extra bold, 900/black
- `font-style: value;` here value can be italic/normal/oblique
- `font-family: value;` here value can be any valid font name. In the following example paragaph will have Times New Roman as its font; if Times New Roman is not available then Times will be applied and if Times is not available then serif font will be applied. This process is known as fallback.

  ```css
  p {
    font-size: 2rem;
    font-weight: bold;
    font-style: italic;
    font-family: "Times New Roman", Times, serif;
  }
  ```

- Use google font: https://fonts.google.com/

### [3.2 Color](https://youtu.be/5_1AKxsu3-I)

- `color: value;` here value can be any color names, hexadcimal colors value, RGB(Red, Green, Blue) color value, hsl (Hue, Saturation, Lightness) value
- Color Name: we can use color names directly as shown below:

  ```css
  p {
    color: green;
  }
  ```

- RGB: we can use Red, Green, Blue values as shown below:

  ```css
  p {
    color: rgb(0, 255, 0);
  }
  ```

- Hexadecimal color: It is a code consist of 6 characters where first 2 characters for Red, Next 2 for Green and last 2 characters for Blue. Example is given below:

  ```css
  p {
    color: #00ff00;
    /*we can write one value instead of two similar values*/
    color: #0f0;
  }
  ```

- Important Tools:
  - Color Picker: https://htmlcolorcodes.com/color-picker/
  - Image color picker: https://imagecolorpicker.com/en
  - How to use colorzilla plugin, how to use
    https://flatuicolors.com/

### [3.3 Text styling](https://youtu.be/oAepBeB_7OU)

- `text-align: value;` here value can be center / left / right / justify
- `text-transform: value;` here value can be uppercase / lowercase / capitalize
- `text-decoration: value;` here value can be underline / overline / line-through / none
- `text-shadow: value;` here value can be x axis, y axis, colorName
- `text-indent: value;`
- `letter-spacing: value;`
- `word-spacing: value;`
- `line-height: value;`  
   Example

  ```css
  p {
    text-align: justify;
    text-decoration: underline;
    text-transform: uppercase;
    letter-spacing: 0.1rem;
    word-spacing: 0.2rem;
    line-height: 1rem;
    text-shadow: 0.1rem 0.1rem green;
  }
  ```

### [3.3 Icon & emoji styling](https://youtu.be/7teTdhRIOCE)

- Get emoji from here: https://unicode-table.com/en/
- Get icon from here: https://www.iconfinder.com/

  ```html
  <style>
    span {
      color: red;
      font-size: 2rem;
    }
  </style>

  <p>I <span> ♥ </span> Bangladesh</p>
  ```

- How to use font awesome icons
  - get font awesome icons here: https://fontawesome.com/
  - get font awesome cdn from here: https://cdnjs.com/libraries/font-awesome
  - add the font awesome cdn inside the html head tag and then you are ready to use font awesome icon  
    Example
    ```html
    <i class="far fa-address-card"></i>
    <i style="color: red;" class="far fa-address-card fa-2x"></i>
    ```
