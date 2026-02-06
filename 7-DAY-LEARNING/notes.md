## Table of contents

- [Day one](#day-one)
- [Day two](#day-two)



## Day one

***CONTENT CATEGORIES***

Content categories are a group of HTML elements which share common characteristics. This use is tell us where an HTML element is expected to appear and define the content model.

There are seven principal categories and four more.

<ol>
    <li>Flow</li>
    <li>Metadata</li>
    <li>Sectioning</li>
    <li>Heading</li>
    <li>Phrasing</li>
    <li>Embedded</li>
    <li>Interactive</li>
    <li>Script supporting</li>
    <li>Form</li>
    <li>Palpable</li>
    <li>Transparent</li>
</ol>

The flow content contain all the rest of categories.

Sectioning and heading are alone

The another big group is the phrasing categorie, which contain, the embedded, metadata and interactive.

[Go back to the table](#table-of-contents)

## Day two

**OUTLINE** the outline of a document is like a strucure compose of principaly the headings and the sections categories.

It's important for keep in mind that you have to use the headings and section in a correct way to have a correct Document outline.

**LANDMARK AND IMPLICIT ROLES** this concept is important because there are many elements which contains by default **rol area** built-in, this roles are called as **landmarks** so is not neccessary to write this attribute again.

**EXAMPLES OF LANDAMARKS**

- banner

- navigation

- main

- complementary

- contentinfo

**Incorrect landmark**

```html

<div role="navigation">

```
```html

<nav>

```

Nav automatically has the role = "navigation" implicity.

The next table shows some key elements and its implicit landmarks.

<table>
  <thead>
    <tr>
      <th>HTML</th>
      <th>Implicit landmark</th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>&lt;header></td>
      <td>banner(Just if it's top level)</td>
    </tr>
    <tr>
      <td>&lt;nav></td>
      <td>navigation</td>
    </tr>
    <tr>
      <td>&lt;main></td>
      <td>main</td>
    </tr>
    <tr>
      <td>&lt;aside></td>
      <td>complementary</td>
    </tr>
    <tr>
      <td>&lt;footer></td>
      <td>contentinfo(if it's top level)</td>
    </tr>
    <tr>
      <td>&lt;form></td>
      <td>form(if it has accessible name)</td>
    </tr>
    <tr>
      <td>&lt;section></td>
      <td>anything</td>
    </tr>
    <tr>
      <td>&lt;article></td>
      <td>anything</td>
    </tr>
    <tr>
      <td>&lt;div></td>
      <td>anything</td>
    </tr>
  
  <tbody/>

</table>

So it's really important yo say that, both ***header*** and ***footer*** are just landmarks if they are at the top level it means if they two are direct childrens of ***body*** element. If they are inside a section they are no longer or don't have a landmark. 

```html

<body>
  <header> <!-- banner ✔ -->


```

Just can exist one ***main*** element in the document.

And section is not a landmark element.

**MEMORIZABLE PHRASES**

First of all, semantic HTML and if this is not sufficient, use **ARIA**.

No ARIA is better than bad ARIA.


**LOGIC ORDER OF THE DOM**

The next could be an example of an correct order of a document.

```html

<header>Header</header>
<nav>Navigation</nav>
<main>Main content</main>
<aside>Related</aside>
<footer>Footer</footer>

```

The DOM order define the lecture order, focus and navigation. The design never has to break this order.

[Go back to the table](#table-of-contents)

## Day 3


