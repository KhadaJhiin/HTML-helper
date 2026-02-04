## Table of Contents
 - [HTML as structural language](#html-as-structural-language-not-a-visual-one)
   - [HTML Elements reference]()
   - [Content categories](#content-categories)
     - [1 - Metadata content](#1-metadata-content)
     - [2 - Flow content](#2-flow-content)
     - [3 - Sectioning content](#3-sectioning-content)
     - [4 - Heading content](#4-heading-content)
     - [5 - Phrasing content](#5-phrasing-content)
     - [6 - Embedded content](#6---embedded-content)
     - [7 - Interactive content](#7---interactive-content)
     - [8 - Palpable content](#8---palpable-content)
     - [9 - Script supporting elements](#9---script-supporting-elements)
   - [Content model](#content-model)
     - [Permitted content](#permitted-content)
     - [Permitted parents](#permitted-parents)


# HTML as structural language not a visual one

## HTML elements reference

In this section we're going to find all the HTML elements with their description and functionality.

[Link to HTML reference page](https://developer.mozilla.org/es/docs/Web/HTML/Reference/Elements)

## Content categories

The **content categories** group HTML elements which share common characteristics.

The content categories are use to define the **content model of elements**, in other words what each element can take as descendents.

There are **seven** content categories, as we can see in the image below. 

![contentCategories](https://developer.mozilla.org/en-US/docs/Web/HTML/Guides/Content_categories/content_categories_venn.png)

### 1 Metadata content

The **metadata** content category modify the presentation or behavior of the rest of the document.

All the elements in the **&lt;head>** include &lt;link>, &lt;style>, &lt;base>, is metadata content. There is a element &lt;meta> for metadata that cannot represented by these other elements.

The metadata elements are:

 <ol>
    <li>&lt;base></li>
    <li>&lt;link></li>
    <li>&lt;meta></li>
    <li>&lt;noscript></li>
    <li>&lt;script></li>
    <li>&lt;style></li>
    <li>&lt;template></li>
    <li>&lt;title></li>
 </ol>

### 2 Flow content

Flow content is a broad category that encompasses most elements that can go inside the &lt;body> element.

The flow elements are :

  <ol>
        <li>&lt;a>   </li>          
        <li>&lt;abbr></li>
        <li>&lt;address></li>
        <li>&lt;article></li>
        <li>&lt;aside></li>
        <li>&lt;audio></li>
        <li>&lt;b></li>
        <li>&lt;bdi></li>
        <li>&lt;bdo></li>
        <li>&lt;blockquote></li>
        <li>&lt;br></li>
        <li>&lt;button></li>
        <li>&lt;canvas></li>
        <li>&lt;cite></li>
        <li>&lt;code></li>
        <li>&lt;data></li>
        <li>&lt;datalist></li>
        <li>&lt;del></li>
        <li>&lt;details></li>
        <li>&lt;dfn></li>
        <li>&lt;dialog></li>
        <li>&lt;div></li>
        <li>&lt;dl></li>
        <li>&lt;em></li>
        <li>&lt;embed></li>
        <li>&lt;fieldset></li>
        <li>&lt;figure></li>
        <li>&lt;footer></li>
        <li>&lt;form></li>
        <li>&lt;h1> - &lt;h6></li>
        <li>&lt;header></li>
        <li>&lt;hgroup></li>
        <li>&lt;hr></li>
        <li>&lt;i></li>
        <li>&lt;iframe></li>
        <li>&lt;img></li>
        <li>&lt;input></li>
        <li>&lt;ins></li>
        <li>&lt;kbd></li>
        <li>&lt;label></li>
        <li>&lt;main></li>
        <li>&lt;map></li>
        <li>&lt;mark></li>
        <li>&lt;math></li>
        <li>&lt;menu></li>
        <li>&lt;meter></li>
        <li>&lt;nav></li>
        <li>&lt;noscript></li>
        <li>&lt;object></li>
        <li>&lt;ol></li>
        <li>&lt;output></li>
        <li>&lt;p></li>
        <li>&lt;picture></li>
        <li>&lt;pre></li>
        <li>&lt;progress></li>
        <li>&lt;q></li>
        <li>&lt;ruby></li>
        <li>&lt;s></li>
        <li>&lt;samp></li>
        <li>&lt;script></li>
        <li>&lt;search></li>
        <li>&lt;section></li>
        <li>&lt;select></li>
        <li>&lt;slot></li>
        <li>&lt;small></li>
        <li>&lt;span></li>
        <li>&lt;strong></li>
        <li>&lt;sub></li>
        <li>&lt;sup></li>
        <li>&lt;svg></li>
        <li>&lt;table></li>
        <li>&lt;template></li>
        <li>&lt;textarea></li>
        <li>&lt;time></li>
        <li>&lt;u></li>
        <li>&lt;ul></li>
        <li>&lt;var></li>
        <li>&lt;video></li>
        <li>&lt;wbr></li>
        <li>&lt;Autonomous custom elements></li>
        <li>&lt;Plain text></li>
  </ol>

A few other elements belong to this category, buy only if a specific condition is fulfilled.

 - &lt;area>, if it is a descendant of a &lt;map> element

  - &lt;link>, if the itemprop attribute is present

  - &lt;meta>, if the itemprop attribute is present

### 3 Sectioning content

Sectioning content, a subset of flow content, creates a section in the current outline defining scope of &lt;header> and &lt;footer> elements.

The section elements are : 

<ol>
    <li>&lt;article></li>
    <li>&lt;aside></li>
    <li>&lt;nav></li>
    <li>&lt;section></li>
</ol>

Sectioning content is a group of HTML elements whose job is to:

  - Split a page into meaningful sections
  - Define the document outline (Structure)
  - Control what a &lt;header> or &lt;footer> belongs to.

```html

<body>
  <header>Site header</header>

  <article>
    <header>Article header</header>
    <p>Article content</p>
    <footer>Article footer</footer>
  </article>

  <footer>Site footer</footer>
</body>


```

### 4 Heading content

Heading content, a subset of flow content, defines the title of a section. This definition applies both to sections marked by an explicit sectioning content elements and to those implicity by the heading content itself.

The heading elements are : 

  <ol>
    <li>&lt;h1> - &lt;h6></li>
    <li>&lt;hgroup></li>
  </ol>

### 5 Phrasing content

Phrasing content refers to the text and markup within a document. Sequences of phrasing content make up paragraphs.

The phrasing content are :

 <ol>
    <li>&lt;abbr>
    <li>&lt;audio>
    <li>&lt;b>
    <li>&lt;bdi>
    <li>&lt;bdo>
    <li>&lt;br>
    <li>&lt;button>
    <li>&lt;canvas>
    <li>&lt;cite>
    <li>&lt;code>
    <li>&lt;data>
    <li>&lt;datalist>
    <li>&lt;dfn>
    <li>&lt;em>
    <li>&lt;embed>
    <li>&lt;i>
    <li>&lt;iframe>
    <li>&lt;img>
    <li>&lt;input>
    <li>&lt;kbd>
    <li>&lt;label>
    <li>&lt;mark>
    <li>&lt;math>
    <li>&lt;meter>
    <li>&lt;noscript>
    <li>&lt;object>
    <li>&lt;output>
    <li>&lt;picture>
    <li>&lt;progress>
    <li>&lt;q>
    <li>&lt;ruby>
    <li>&lt;s>
    <li>&lt;samp>
    <li>&lt;script>
    <li>&lt;select>
    <li>&lt;slot>
    <li>&lt;small>
    <li>&lt;span>
    <li>&lt;strong>
    <li>&lt;sub>
    <li>&lt;sup>
    <li>&lt;svg>
    <li>&lt;template>
    <li>&lt;textarea>
    <li>&lt;time>
    <li>&lt;u>
    <li>&lt;var>
    <li>&lt;video>
    <li>&lt;wbr>
    <li>Autonomous custom elements
    <li>Plain text
 </ol>

 A few other elements belong to this category, but only if a specific condition is fulfilled:

 - &lt;a>, if it contains only phrasing content
 - &lt;area>, if it is a descendant of a &lt;map> element
 - &lt;del>, if it contains only phrasing content
 - &lt;ins>, if it contains only phrasing content
 - &lt;link>, if the itemprop attribute is present
 - &lt;map>, if it contains only phrasing content
 - &lt;meta>, if the itemprop attribute is present

### 6 - Embedded content

Embedded content, a subset of flow content, imports another resource or inserts content from another markup language or namespace into the document.

The embedded content elements are:

<ol>
    <li>&lt;audio>
    <li>&lt;canvas>
    <li>&lt;embed>
    <li>&lt;iframe>
    <li>&lt;img>
    <li>&lt;math>
    <li>&lt;object>
    <li>&lt;picture>
    <li>&lt;svg>
    <li>&lt;video>
</ol>

### 7 - Interactive Content

Interactive content, a subset of flow content, includes elements that are specifically designed for user interaction.

The interactive content elements are:

<ol>
    <li>&lt;button>
    <li>&lt;details>
    <li>&lt;embed>
    <li>&lt;iframe>
    <li>&lt;label>
    <li>&lt;select>
    <li>&lt;textarea>
</ol>


Some elements belong to this category only under specific conditions:

 - &lt;a>, if the href attribute is present
 - &lt;audio>, if the controls attribute is present
 - &lt;img>, if the usemap attribute is present
 - &lt;input>, if the type attribute is not in the hidden state
 - &lt;object>, if the usemap attribute is present
 - &lt;video>, if the controls attribute is present

### 8 - Palpable content

This categorie groups content that the user really perceives, that means content that is rendered, is not empty is not hidden and gives something real to the user like, text, images, control etc.

The palpable elements are:

<ol>
    <li>&lt;a>
    <li>&lt;abbr>
    <li>&lt;address>
    <li>&lt;article>
    <li>&lt;aside>
    <li>&lt;b>
    <li>&lt;bdi>
    <li>&lt;bdo>
    <li>&lt;blockquote>
    <li>&lt;button>
    <li>&lt;canvas>
    <li>&lt;cite>
    <li>&lt;code>
    <li>&lt;data>
    <li>&lt;del>
    <li>&lt;details>
    <li>&lt;dfn>
    <li>&lt;div>
    <li>&lt;em>
    <li>&lt;embed>
    <li>&lt;fieldset>
    <li>&lt;footer>
    <li>&lt;figure>
    <li>&lt;form>
    <li>&lt;iframe>
    <li>&lt;img>
    <li>&lt;ins>
    <li>&lt;kbd>
    <li>&lt;label>
    <li>&lt;main>
    <li>&lt;map>
    <li>&lt;mark>
    <li>&lt;math>
    <li>&lt;meter>
    <li>&lt;nav>
    <li>&lt;object>
    <li>&lt;p>
    <li>&lt;picture>
    <li>&lt;pre>
    <li>&lt;progress>
    <li>&lt;q>
    <li>&lt;ruby>
    <li>&lt;s>
    <li>&lt;samp>
    <li>&lt;search>
    <li>&lt;section>
    <li>&lt;select>
    <li>&lt;small>
    <li>&lt;span>
    <li>&lt;strong>
    <li>&lt;sub>
    <li>&lt;sup>
    <li>&lt;svg>
    <li>&lt;table>
    <li>&lt;textarea>
    <li>&lt;time>
    <li>&lt;u>
    <li>&lt;var>
    <li>&lt;video>
    <li>Autonomous custom elements
    <li>Plain text that is not inter-element whitespace
</ol>

Some elements belong to this category only under specific conditions:

- &lt;audio>, if the controls attribute is present
- &lt;dl>, if the element's children include at least one name-value group
- &lt;input>, if the type attribute is not in the hidden state
- &lt;ol>, if it's children include at least one &lt;li> element
- &lt;ul>, if it's children include at least one &lt;li> element

### 9 - Script-supporting elements

Script-supporting elements are elements that don't directly contribute to a document's rendered output. Instead, they serve to support scripts, either by containing or specifying script code directly or by specifying data that will be used by scripts. Nearly all elements, including those that only take specific elements (such as &lt;ul>, which takes &lt;li> elements), can contain script-supporting elements.

The script-supporting elements are:

 - &lt;script>
 - &lt;template>

### 10 - Form-associated content

Form-associated content is a subset of flow content comprising elements that have a form owner and can be used everywhere flow content is expected. A form owner is either the containing &lt;form> element or the &lt;form> whose id is specified in the element's form attribute.

The form-associated elements are:

 - &lt;button>
 - &lt;fieldset>
 - &lt;input>
 - &lt;object>
 - &lt;output>
 - &lt;select>
 - &lt;textarea>
 - &lt;img>

This category contains several sub-categories:

listed
Elements that are listed in the HTMLFormElement.elements and HTMLFieldSetElement.elements collections. Includes &lt;button>, &lt;fieldset>, &lt;input>, &lt;object>, &lt;output>, &lt;select>, and &lt;textarea>.

submittable
Elements that can be used for constructing the form data set when the form is submitted. Includes &lt;button>, &lt;input>, &lt;select>, and &lt;textarea>.

resettable
Elements that can be affected when a form is reset. Includes &lt;input>, &lt;output>, &lt;select>, and &lt;textarea>.

autocapitalize-and-autocorrect-inheriting
Elements that inherit the autocapitalize and autocorrect attributes from their form owner. Includes &lt;button>, &lt;fieldset>, &lt;input>, &lt;output>, &lt;select>, and &lt;textarea>.

labelable
Elements that can be associated with &lt;label> elements. Includes &lt;button>, &lt;input> (all types other than hidden), &lt;meter>, &lt;output>, &lt;progress>, &lt;select>, and &lt;textarea>.

### Transparent content model

In addition to the listed content categories, an element's content model may also be defined as "transparent". If an element X's permitted content is "transparent", then we look at the parent of X. We intersect the permitted content of X's parent with the content categories of X, and the result is what "transparent" means in this context. If the parent of X also has a transparent content model, then we continue up the tree until we find a non-transparent content model. When there's no such parent, "transparent" means "flow content".

For example, a &lt;ruby> element accepts phrasing content. The &lt;ins> element is of category phrasing content when it contains only phrasing content. Therefore, an &lt;ins> element can be placed inside a &lt;ruby> element. The &lt;ins> element's permitted content is "transparent", which when nested in &lt;ruby> means "phrasing content". However, &lt;rt> elements are not phrasing content. Therefore, an &lt;rt> element cannot be nested inside this &lt;ins> element, even though both &lt;rt> and &lt;ins> can be inside &lt;ruby>, and &lt;ins> is "transparent".

```html

This is an example of wrong code

<ruby>
  Text before
  <ins>
    <!-- Invalid: rt cannot be placed inside ins here -->
    <rt>Pronunciation</rt>
  </ins>
</ruby>

```

```html

This is an example of good code

<ruby>
  Text before
  <!-- Valid: ins can be inside ruby, and rt can be inside ruby -->
  <ins>Inserted text</ins>
  <rt>Pronunciation</rt>
</ruby>

```

```html

Good code

<ruby>
  Text before
  <!-- Valid: rt can be inside ruby, and ins can be inside rt -->
  <rt><ins>Pronunciation</ins></rt>
</ruby>

```

Transparent is a content model, not a content category, so it only defines what an element can contain, not where the element can be placed. That is, when determining an element's children's licitness, you cannot "see through" transparent children. For example, a &lt;ul> element accepts only &lt;li> elements and script-supporting elements, and does not allow &lt;del> or &lt;ins>, even if the &lt;del> only contains &lt;li> elements.

```html

Bad content

<ul>
  <del>
    <li>Oranges</li>
    <li>Toilet paper</li>
  </del>
  <li>Toothpaste</li>
</ul>

```

```html

Good code

<ul>
  <li><del>Oranges</del></li>
  <li><del>Toilet paper</del></li>
  <li>Toothpaste</li>
</ul>

```

[⬆ Back to table of contents](#table-of-contents)

## Content Model

The content model is whay kind of element can contain another element but talking about catogories, is abstract basing on categories, example:

 - This element just can contain **flow content**

### Permitted content

Now we also have the **permited content** which is the application of the content model, here we start to talking about HTML elements.

  - **X HTML element can contain** : p, section, article, ul etc...

### Permitted parents

The permitted parents is similar to the Permitted content is what HTML tags the element can have as parents.

This is like the grammar of HTML, because this language has rules, you have to know them although the browser forgive you the mistakes, the validator and accessibility technology don't do it.







[⬆ Back to table of contents](#table-of-contents)