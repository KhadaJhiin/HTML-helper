## Table of Contents

- [Semantic HTML](#semantic-html)
- [Importance](#importance-of-semantic-html)
  - [Why should you care about Semantic HTML?](#why-should-you-care-about-semantic-html)
  - [Importance of Hierarchy](#importance-of-hierarchy)
  - [Presentational and semantic HTML](#difference-between-presentational-and-semantic-html)
- [Nuanced Semantic Elements](#nuanced-semantic-elements)
  - [Idiomatic](#idiomatic)
  - [Emphasis elements](#emphasis-elements)
  - [Bring attention (b)](#bring-attention)
  - [Description list](#description-list)
- [Working with text and time semantic HTML](#working-with-text-and-time-semantic-html)
  - [Block and inline quotes](#block-and-inline-quotes)
  - [Abbreviations in HTML](#abbreviations-in-html)
  - [Addresses in HTML](#addresses-in-html)
  - [Times and dates in HTML](#times-and-dates-in-html)
- [Specialized semantic elements](#specialized-semantic-elements)
  - [Mathematical Equations](#mathematical-equations)
  - [Computer code](#computer-code-in-html)
  - [U, S and Ruby elements](#u-s-and-ruby-elements)
- [Semantic HTML summary](#semantic-html-summary)

# Semantic HTML

## Importance of semantic HTML

## Why should you care about semantic HTML?

Semantics are the meaning of words, or phrases in a language, You can think of your HTML document like you would text a document. So you have to use, headings, images, bold text and other formatting.

One of the most important property of semantic HTML is that this will ensure the best experience for users with assistive technology like screen readers. But this can also improve your search rankings. This means the SEO.

## Importance of Hierarchy

When we talk about headings, is important put these in a correct hierarchy. It means, first of all a h1 then h2. Use a correct hierarchy improve the SEO and help to the assistive technologies.

Remember don't skip from h1 to h3, if you need something different just choose the correct semantic heading and modify it using CSS.

## Difference between presentational and semantic HTML

Presentational HTML was used before, now in modern HTML this attributes are deprecated, now we set all the styles in CSS.

Now is the **semantic HTML** the recomended practice to create your web page, as we said before it has a lot of advantages in terms on maintenability, understanding and SEO of your pages.

Some exmaples of semantic HTML.

  **Structure tags**

 - header
 - nav
 - main
 - section
 - article
 - aside

 **Text level semantic tags**

 - strong
 - em
 - mark
 - time
 - address

 **Media and content semantic tags**

 - figure and figcaption

The semantic HTML crearly show their purpose within the HTML structure.

A common doubt can be the difference between **section** and **article**.

 - **Article :** The article has self-contained content, it's independent, this means that it makes sense outside the page or site, some examples.
    - Blog posts
    - News articles
    - Product cards
    - Forum posts
    - Comments
    - Social media posts

```html
  <article>
    <h2>How to Learn HTML</h2>
    <p>This article explains the basics of HTML.</p>
  </article>

```

  You could show this ina blog, on a homepage preview and it still works.

  - **Section :** Section depends on the context of the page for example.

    - About
    - Services
    - Contact

  These sections cannot works on its own, because you cannot put a section services without a context.


[⬆ Back to Table of Contents](#table-of-contents)



## Nuanced semantic elements

## Emphasis elements

There are some tags using to give relevance to some words. In this case we are going to talk about someones.

### Idiomatic

This tag is frequently used for highlighting alternative voice or mood, idiomatic terms from another language, technical terms, and thoughts.

```html

<p>There is a certain <i lang="fr">je ne sais quoi</i> in the air.</p>

```

We can see that inside the open **i** tag, we can set the language of the phrase in this case the phrase is written in French.

The **i** element doesn't indicate if the text is important or not, it only shows that it's somehow different from the surrounding text.

### Emphasis element

This is used in parts of the text where you need special emphasis.

```html

<p>
  Never give up on <em>your</em> dreams.
</p>

```

Is important to know that, if the text just need to be italized to visual purposes, you just should use CSS instead these tags, remember that the use of this tags is to give more importance than the text sourronding.

[⬆ Back to Table of Contents](#table-of-contents)

## Bring attention

The **Bring attention to** element or &lt;b> element is used with visual purposes to catch attention in the text displayed on the screem.

In the other hand we have the **strong** element or &lt;strong> element, which have a more semantic meaning than the other one, it gives a sense of urgency, represent that the text is crucial its work is not just visual.

## Description list

This type of list are perfect to presenting terms and definitions in an organized and easy-to-read format, like in a glossary, or real dictionary, when you can find words with their corresponding definitions.

```html

<dl>
  <dt>HTML</dt>
  <dd>HyperText Markup Language</dd>
  <dt>CSS</dt>
  <dd>Cascading Style Sheets</dd>
</dl>

```

The meaning of each tag are.

 - **dl** : Description list
 - **dt** : Description term
 - **dd** : Description details

[⬆ Back to Table of Contents](#table-of-contents)

## Working with text and time semantic HTML

### Block and inline quotes 

This quotes are commonly used when you have to cite a section or text from another source. If this quote has an address you can cite the address as follow.

```html

<blockquote cite="https://www.freecodecamp.org/news/learn-to-code-book/">
  "Can you imagine what it would be like to be a successful developer? To have built software systems that people rely upon?"
</blockquote>

```

It is important to understand that you have to put the "" if you want to show these quotes in your text, also you can put more than one pharagraph inside your blockquote element, it's helpful if you want to group more than one pharagraph inside the same block.

```html

<blockquote cite="https://www.freecodecamp.org/news/learn-to-code-book/">
  <p>Build your projects. Show them to your friends. Build projects for your friends.</p>
  <p>Build your network. Help the people you meet along the way. What goes around comes around. You'll get what's coming to you.</p>   
  <p>It is not too late. Life is long.</p>
  <p>You will look back on this moment years from now and be glad you made a move.</p>
</blockquote>

```

You can also show the cite outsite to the users, it means to be show in the screem.

Remember that these two **cite** are differents, the first one is an attribute which just works behind the scenes. The second one is an HTML element which is show on the screem.

```html

<div>
  <blockquote cite="https://www.freecodecamp.org/news/learn-to-code-book/">
    Can you imagine what it would be like to be a successful developer? To have built software systems that people rely upon?
  </blockquote>
  <p>—Quincy Larson, <cite>How to Learn to Code and Get a Developer Job [Full Book].</cite></p>
</div>

```

**Inline quotation**

If you want to write a short quote, you should use the **q** as follow.

```html
<p>
  As Quincy Larson said,
  <q cite="https://www.freecodecamp.org/news/learn-to-code-book/">
    Momentum is everything.
  </q>
</p>

```
### Abbreviations in HTML

There are two common forms or abbreviations: **Acronyms** and **initialisms.**

**ACRONYSM :** An acronyms is a word formed from the initial letters of a phrase, with each letter representing the first letter of a word in that phrase.

***GUI*** is an example of an acronysm. It stands for **Graphical User Interface**.


**INITIALISM :** Is almost the same, the word is formed by the initial letter of a phrase.

***HTML*** stands for **Hyper text markup language**

The main difference is that the **Acronysm** is pronounced as a normal word and the **Initialism** is pronounced by spelling out each letter.

If you need to put abrevations, you can use the **abbr** tag, and is opcional but if you add the attribute **title** when the user put his cursor over the text, is going to appear a text with  the title.

```html

<p><abbr title="HyperText Markup Language">HTML</abbr> is the foundation of the web.</p>

```


### Addresses in HTML

This is recomended to use for example when you are making a web page and is time to start with the contact section.

```html

<address>
  <h2>Company Name</h2>
  <p>
    1234 Elm Street<br />
    Springfield, IL 62701<br />
    United States
  </p>
  <p>Phone: <a href="tel:+15555555555">+1 (555) 555-5555</a></p>
  <p>Email: <a href="mailto:contact@company.com">contact@company.com</a></p>
</address>

```

### Times and Dates in HTML

This is use to represent time and dates.

```html

<p>The reservations are for <time datetime="20:00">20:00 </time></p>


```

The **datatime** attribute is used to translate dates an time into a machine-readble format.

```html
<p>
  The graduation will be on <time datetime="2024-06-15T15:00">June 15</time>
</p>

```

The letter T between the date and the hours represents the separation between they two.

Whenever you need to represent events, publication dates, or appointments, it is best to use the time element.

[⬆ Back to Table of Contents](#table-of-contents)

## Specialized semantic elements

### Mathematical equations

The first special element is the sup element, to put a letter above the normal line of text.

```html

<p>2<sup>2</sup> (2 squared) is 4.</p>

<p>
  Monseigneur is often written as <strong>M<sup>gr</sup></strong>.
</p>

```

The other case is the subscript element to show the elements under the normal line of text.

```html

<p>CO<sub>2</sub></p>

```

### Computer code in HTML

To represent code in your HTML you have to use the **code** tag. This tag is used to represent code inline, as follow.

```html

<p>
  To set the text color to blue in CSS, use the following code:
  <code>color: blue;</code>
</p>

```

If you want to show or put more than one line of code have to use the nex configuration.

```html

<pre>
  <code>
    body {
      color: red;
    }
  </code>
</pre>

```

### U S and ruby elements.

The **U** which stands for *unarticulated annotation* element is used for represent text that has non-textual annotation aplied in other words it means that the underline text is not just a decoration, the U is saying, that text means something. For example to show that some text is incorrect.

```html

<p>
  You can use the unarticulated annotation element to highlight
  <u>inccccort</u> <u>spling</u> <u>issses</u>.
</p>

```

The default styling for the u element is a black underline underneath the text.
In the case before we can see that the words are misspelled. Or as we said before the meaning besides the visual underlined is "This text is wrong"

The **S** which stands for strikethrough element, means that the text is no longer accurate or relevant. 
Here is an example of using the S to show the cancellation of an activity.

```html

  <p><s>Tomorrow's hike will be meeting at noon.</s></p>

  <p>Due to unforeseen weather conditions, the hike has been canceled.</p>

```

Visually we say the sentence crossed out by a line.

The **Ruby** element represents small text shown above or below the main text. It is typically used to show the pronunciation of East Asian characters.

```html
  <ruby> 明日 <rp>(</rp><rt>Ashita</rt><rp>)</rp> </ruby>

```
The **rp** element, or ruby fallback parenthesis element, is used as a fallback for browsers lacking support for displaying ruby annotations.

The **rt** element, or ruby text element, is used to indicate text for the ruby annotation. This text is usually used for pronunciation, or translation details in East Asian typography.

While the ruby element can be used for other types of annotations, the most common use case is for East Asian typography.

[⬆ Back to Table of Contents](#table-of-contents)

## Semantic HTML summary

In the following link we are going to find a summary of all the topics saw in this section

[Summary of semantic HTML](https://www.freecodecamp.org/learn/responsive-web-design-v9/review-semantic-html/review-semantic-html)


[⬆ Back to Table of Contents](#table-of-contents)