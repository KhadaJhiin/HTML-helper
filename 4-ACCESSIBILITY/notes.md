## Table of contents

- [Accessibility](#accessibility)
  - [What is accessibility](#what-is-accessibility)
- [Screen readers](#screen-readers)
- [Auditing tools for accessibility](#accessibility-auditing-tools)
- [Accessibility and best practices tables](#accessibility-and-best-practices-for-tables)
- [Associated label for inputs](#associated-label-for-inputs)
- [WAI-ARIA](#wai-aria)
  - [Document structure roles](#document-structure-roles)
  - [Widget](#widget)
  - [Land mark](#landmark-roles)
  - [Live regions](#live-regions)
  - [Windows roles](#windows-role)
- [Aria label](#aria-label)
- [Aria labelledby](#aria-labelledby)
- [Aria-hidden](#aria-hidden)
- [Aria-describedby](#aria-described-by)
- [Alt attribute](#alt-attribute)
- [Link text](#link-text)
- [Video and audio accessible](#video-and-audio-accessible)
- [Keyboard Navigation](#keyboard-navigation)
- [Summarize accessility](#summarize)
- [HTML REVIEW]()
 

# Accessibility

## What is accessibility

Accessibility involves creating products and services that everyone can use. In the context of web development, it's making websites that everyone can understand and interact with.

When we talking about website that everyone can understand we're including people with some disabilities as blindness, low vision, deafness etc.

In order to improve the experience of these people while they're using a web page the W3C which stands for (World wide web consortium) develop a set of international standards that you can follow to make your websites more accessible and easier to use for people with disabilities.

The standards are known as the "Web content accessibility guidelines (WCAG).

These guidelines are designes with four core principles in mind, known as **POUR**.

 - P stands for *Perceivable* : Users must be able to preceive the information that you are presenting. For example you can provide alternative text for images, so users who access your website with a screen reader can understand them.

 - O stands for *Operable* : Users must be able to operate through your page using for example the keyboard, insted just using the mouse.

 - U stands for *Understandable* : Users must be able to understand the information. For example, you can avoid complex sentences and use simple language as much as possible.

 - R stands for *Robust* : A wide range of browsers and other tools, including assistive techonologies, must be able to interpret the content.

To check if you are following these guidelines correctly, you can access the Quick reference of the World Wide Web Consortium. There you will find a comprenhensive list of criterie and techniques.

[⬆ Back to Table of Contents](#table-of-contents)

## Screen readers

Screen reader are assistive technology programs that help blind people and visually impaired people use computers and mobile devices.

There's a misconception that screen readers are text-to-speech devices, there're even some screen readers that renders text to braille. 

[⬆ Back to Table of Contents](#table-of-contents)

## Accessibility auditing tools

There're some tools made for test your web pages o app in order to give you a feedback related to accessibility.

 - **Lighthouse** : You can check SEO, best practices accessibility and performance.
    *intructions* : *To use Lighthouse, open your DevTools by pressing F12 and switching to the Lighthouse tab. Select the metrics you want to check, choose the device you want to test on, and click the "Analyze page load" button.*
 - **Lighthouse web version** : This app version web gives you a better analize of your content. [Link to the web](https://pagespeed.web.dev/)

 - **WAVE** : WAVE is another reliable accessibility checker you can use as a Chrome extension or on the web. All you need to do is enter the URL of your website and a comprehensive accessibility report will be generated for you. This report includes accessibility features implemented, ARIA, and contrasts.

 - **The IBM Equal Accessibility Checker** : is another robust tool for improving digital content accessibility. With it, you can scan your websites for accessibility issues and generate a detailed report.

You can use it as a Chrome extension or Firefox add-on.

To use the IBM Accessibility Checker as a Chrome extension, download it from the Chrome web store. Open your Devtools by pressing F12 and selecting the "Accessibility Checker" tab located in the Elements panel. Click the scan button to start the check and a report will be generated for you. You can export the report as a spreadsheet and an HTML file by clicking the "Export XLS" button.

[⬆ Back to Table of Contents](#table-of-contents)

## Accessibility and best practices for tables

There are a lot of recomendations to make your tables more acesibles, for example.

 - **Use caption to give a title to your table.**

 ```html

 <table>
     <caption>Our Pets</caption>
  <!-- Table Rows and Columns -->
</table>
 
 ```

 - **Use of header for columns or rows.**
    You can set with th headers in rows or columns to show what each column or row represent.

 ```html

 <table>
     <caption>Our Pets</caption>
  <thead>
      <tr>
      <!-- Column Headers -->
      <th>Name</th>
      <th>Age</th>
      <th>Type</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Nora</th> <!-- Row Header -->
      <td>5</td>
      <td>Dog</td>
    </tr>
    <tr>
        <th>Gino</th> <!-- Row Header -->
      <td>2</td>
      <td>Cat</td>
    </tr>
  </tbody>
 </table>
 
 ```
 - **Scope**

 You can use scope who indicates to the scream readers if a element of the table is a column or a row. 

 ```html

 <table>
     <caption>Our Pets</caption>
  <thead>
      <tr>
      <!-- Now they have scope -->
      <th scope="col">Name</th>
      <th scope="col">Age</th>
      <th scope="col">Type</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">Nora</th>
      <td>5</td>
      <td>Dog</td>
    </tr>
    <tr>
        <th scope="row">Gino</th>
      <td>2</td>
      <td>Cat</td>
    </tr>
  </tbody>
 </table>
 
 ```

 If a column or row header spans across multiple cells, the scope will also be applied to each one of the cells individually. Here's an example of that:

 ```html

 <table>
  <tbody>
      <tr>
      <td></td>
      <th scope="col">Name</th>
      <th scope="col">Age</th>
    </tr>
    <tr>
      <th rowspan="2" scope="row">Dogs</th>
      <th scope="row">Nora</th>
      <td>5</td>
    </tr>
    <tr>
        <th scope="row">Gino</th>
      <td>2</td>
    </tr>
    <tr>
      <th rowspan="2" scope="row">Cats</th>
      <th scope="row">Lulu</th>
      <td>10</td>
    </tr>
    <tr>
      <th scope="row">Elizabeth</th>
      <td>6</td>
    </tr>
  </tbody>
 </table>
 
 ```

[⬆ Back to Table of Contents](#table-of-contents)

## Associated label for inputs.

The best practice is associate inputs using labels and the property for. This practice is also important to inprove the SEO of the page.

```html

<form>
  <label for="name">Your Name</label>
   <input type="text" id="name" />
</form>


```


[⬆ Back to Table of Contents](#table-of-contents)


## WAI-ARIA

WAI-ARIA stands for **(Web accessibility Initiative-Accessible Rich Internet Applications)**. The difference between WCAG and WAI-ARIA is that WCAG gives general guidelines for web accessibility and WAI-AREA gives specific rules for making dynamic and interactive content accessible for users of assistive technologies.

So, the primary purpose of WAI-ARIA is to improve accessibility for dynamic content and UI components that do not have native HTML equivalents.

WAI-ARIA works by introducing a set of attributes you can add to HTML elements to provide additional semantic information. These attributes are categorized into roles, states, and properties.

**ARIA role** defines the purpose of an element within a website or web app. Here is an example of setting the role to button for a div element.

```html

<div role="button">Click Me</div>

```

We have to keep in mind that this is just informative and it will be just using to assistive technologies, it means that if you put the role button to that div, that div is not going to behave like a button. 

ARIA properties provide additional details about elements. For example, the **aria-labelledby** property lets you connect an element to a specific label:

```html

<h2 id="header-id">About freeCodeCamp</h2>
<button id="button-id" aria-labelledby="header-id button-id">Learn More</button>

```

To get the best out of WAI-ARIA, try to stick with native HTML whenever possible since it generally provides more accessibility out of the box.

Use WAI-ARIA only when HTML falls short, and don’t forget to test with assistive technologies like screen readers, or have people with disabilities test your work. Also, make sure your WAI-ARIA states and properties update with the content in real time. Avoid overusing ARIA, as it can often be confusing.

ARIA roles specify the semantic meaning of HTML elements. They're essential for making web content accessible to people who use assistive technologies, like screen readers.

HTML has semantic and non-semantic elements, based on whether they convey meaning about their content.

Many semantic HTML elements already have an ARIA role assigned by default. For example, the button element has a default ARIA role of button.

But non-semantic elements don't have a role. For example, screen readers will not know how to interpret the purpose of a div if you don't specify its role explicitly.

To specify the ARIA role of an element, you just need to add the role attribute, like this role="ARIA role", where value is the name of a role in the ARIA specification.

Here is an example of using the role attribute with a value of "alert":

```html

<link rel="stylesheet" href="styles.css">

<div class="alert" id="exp-warning" role="alert">
  <span class="hidden">Your log in session will expire in 3 minutes.</span>
</div>

```

There are six main categories of ARIA roles:

 - Document structure roles
 - Widget roles
 - Landmark roles
 - Live region roles
 - Window roles
 - And Abstract roles

[⬆ Back to Table of Contents](#table-of-contents)

## Document structure roles

Document structure roles define the overall structure of the web page. With these roles, assistive technologies can understand the relationships between different sections and help users navigate the content.

However, most of the document structure roles are not used in modern web development because browsers already support equivalent semantic HTML elements, which should be prioritized whenever possible.

You should specify the roles that don't have an equivalent semantic element. For example: toolbar, tooltip, feed, math, presentation, none, and note.

There are other similar roles but these are the most commonly used ones. This is an example of a div with the math ARIA role. The div contains a mathematical equation.

```html

<div role="math" aria-label="x squared + y squared = 3">
  x<sup>2</sup> + y<sup>2</sup> = 3
</div>

```
aria-label attribute. The value of this attribute should be a string that represents the expression.

## Widget

Widget roles define the purpose and functionality of interactive elements, like scrollbars.

Examples of widget roles include scrollbar, searchbox, separator (when focusable), slider, spinbutton, switch, tab, tabpanel, and treeitem.

Here is an example of a searchbox:

```html

<div class="search-container" role="search">
  <label for="searchbox" class="visually-hidden">Search</label>

  <div
    id="searchbox"
    class="searchbox"
    role="searchbox"
    aria-label="Search the site"
    tabindex="0"
    contenteditable="true">
  </div>

  <button type="button" aria-label="Submit search">Search</button>
</div>

```

## Landmark roles

Landmark roles classify and label the primary sections of a web page. Screen readers use them to provide convenient navigation to important sections of a page. You should use them sparingly to keep the overall layout simple and easy to understand. Examples of landmark roles are banner, complementary, contentinfo, form, main, navigation, region, and search. Each of these roles has a corresponding HTML equivalent, such as header, footer, aside, form, main, nav, section, and search. If you use the proper HTML elements to define the sections of your page then it is not necessary to explicitly add the role attribute to these elements.

Here is an example of a banner:

```html

<div role="banner" class="site-banner">
  <h1>Accessible Web Design</h1>
  <nav>
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">Articles</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </nav>
</div>

```

## Live regions

Live region roles define elements with content that will change dynamically. This way, screen readers and other assistive technologies can announce changes to users with visual disabilities. These roles include: alert, log, marquee, status, and timer.

Here is an example of a status:

```html

<div class="status-demo">
  <button id="update-status-btn">Check Status</button>
  <div id="status-msg" role="status" class="status-message">
    No updates yet.
  </div>
</div>

```

## Windows role

Window roles define sub-windows, like pop up modal dialogues. These roles include alertdialog and dialog. Please note that it is now considered a best practice to use the HTML dialog element and its associated JavaScript methods instead of manually creating a dialog.

Here is an example of using a dialog role for a custom dialog:

```html

<button id="open-dialog">Open Dialog</button>

<div id="custom-dialog" role="dialog" aria-modal="true" aria-labelledby="dialog-title" class="dialog">
  <div class="dialog-content">
    <h3 id="dialog-title">Confirm Action</h3>
    <p>Are you sure you want to delete this file?</p>
    <div class="dialog-actions">
      <button id="confirm-btn">Yes</button>
      <button id="close-dialog">Cancel</button>
    </div>
  </div>
</div>

```

[⬆ Back to Table of Contents](#table-of-contents)

## Aria label

aria-label is especially useful for elements that do not have visible text but still need to be described by screen readers. For example, buttons with only icons often need aria-label to convey their purpose.

```html

<button aria-label="Search">
  <i class="fa-solid fa-magnifying-glass"></i>
</button>

```

If the button contained the text "Search" instead of an icon, then there would be no need for the aria-label attribute as the text would provide the label for the button.

For input elements, the aria-label attribute provides a label directly if there isn't a visible label associated with the input.

## Aria labelledby

The aria-labelledby attribute does the exact same thing as the aria-label attribute, but instead of defining the text directly in the attribute, you use a reference to text that already exists on the page. The existing text must have an id attribute, which will be used for the reference value in the aria-labelledby attribute.

```html

<input type="text" aria-labelledby="search-btn">
<button type="button" id="search-btn">Search</button>

```

Combining multiple id values into a single aria-labelledby attribute value is also possible. Here's how that works:

```html

<div>
  <span id="volume-label">Volume</span>
  <span id="volume-details">Adjust the volume level</span>
  <input
    type="range"
    min="0"
    max="100"
    value="30"
    aria-labelledby="volume-label volume-details">
</div>

```

You've seen that both aria-label and aria-labelledby attributes help screen readers understand what elements do. So, which one should you use? Since they both provide the same functionality, either can be used, but there may be a few advantages to using aria-labelledby over aria-label:

If someone is using a translation service to translate the content on your page, the text in an aria-label attribute may not always be translated.
Using aria-labelledby can also help prevent a mismatch between the visible label text and the invisible label for screen reader users since updating the visible text will automatically update the invisible label.
aria-labelledby can make it much easier to programmatically create complex invisible labels consisting of multiple sources of text.
One last note, do not use aria-label and aria-labelledby on an element at the same time. In this case, the invisible label for screen readers will always be determined by aria-labelledby and aria-label will be completely ignored.


[⬆ Back to Table of Contents](#table-of-contents)

## Aria-hidden

Aria-hidden attribute is used to hiden some things to people who use assistive technology, the way how you have to use it is just put the attribute to the HTML element, and set its value to true.

This configuration keeping the elements visible on the page but is omited for screen readers or any others assistive technology. 

Some cases of use can be.

 - Icons and images that only have a decorative purpose
 - Duplicated content

```html

<button>
  <i class="fa-solid fa-gear" aria-hidden="true"></i>
  <span class="label">Settings</span>
</button>

```

You do not have to use aria-hidden in the next three cases.

 - The HTML element already has a hidden attribute.
 - The element or the element's ancestor is already hidden with display: none.
 - The element or the element's ancestor is already hidden with visibility: hidden.

You should also know that setting aria-hidden to false will not expose the element to assistive technologies if any of its parents has this attribute set to true.

[⬆ Back to Table of Contents](#table-of-contents)

## Aria described by

aria-describedby, is use to associate elements in the page, we are going to see some examples to understand the concep.

```html

<form>
  <label for="password">Password:</label>
  <input type="password" id="password" aria-describedby="password-help" />
  <p id="password-help">Your password must be at least 8 characters long.</p>
</form>

```

In this example we are associating the input with de pharagraph, so in some scren readers when the user put the focus on the input the pharagraph with the instructions are going to be read.

The aria-describedby attribute is a powerful attribute that can be used to help ensure that additional information about an element is provided to screen reader users when they interact with the element. It is most commonly used to associate instructions and error messages with form inputs in order to reduce the chance that screen reader users will miss these messages as they navigate the form.

```html

<button aria-describedby="delete-message">Delete</button>

<p id="delete-message">Warning! All deletions are permanent.</p>

```

[⬆ Back to Table of Contents](#table-of-contents)

## Alt attribute

Alt which stands for (Alternative text) is a brief text description of an image. This attribute is essential for people who cannot see maybe an image.

Alternative text is also used by searching engines to understand images.

The alt attribute has to be clear and oriented to the importance of the page, is bad practice just put alt text like "resort" or "pupie in the beach" remeber that it can be used for people who cannot see, so if the image is really important to the content of the page, you have to put a good alt text, for example.

 - "Tropical resort featuring a swimming pool surrounded by palm trees and bungalows."
 - "A black and white puppy with an orange collar lies on its belly in the sand, looking off to the side. A bright orange ball rests near its front paws."

Some goods practices when you use alt text.

 - You should try to keep alt text short. It should be detailed enough to understand the image but not so long that it becomes confusing.
 - You should not try to describe every little detail. Focus on the most important aspects of the image.
 - Generally, you don't need to start with "image of" or "picture of." You can just start the description directly.
 - Also, if there's similar text around the image, you don't need to write it again.
 - It's usually recommended to end the alt text with a period for consistency.
 - If the image is a link to another page, instead of describing the image itself, the alt text should describe what will happen if users click on it.

For example, if your website has a right arrow icon that takes the user to the next page, instead of writing an alt text that only says "right arrow", like in this example, where you can see the alt attribute with this description:

Intead use the next code.

```html

<a href="about.html">
  <img src="arrow-right.png" alt="Right arrow." />
</a>

```

You should use this code.

```html

<a href="about.html">
  <img src="arrow-right.png" alt="Go to next page." />
</a>

```

Just important images have to use alt text, if the imagenes are just decorative you should avoid this alt text and it will be ignored by the screen reader and other assistive technologies.

```html

<img src="decorative_image.jpg" alt="" />

```

All the images should have an alt attribute, so the screen reader que ignored them, if you omited the attribute is probably that the screen reader, read the name of the file and it can be confusing to the users.

[⬆ Back to Table of Contents](#table-of-contents)

## Link text

We're going to see, the benefits of a good link text in the accessibilt field.

For people who don't have any disability is easy to understan maybe a bad link text, but for people for example blind people it is better to use.

"Read our accessibility guide" 

Than.

"Click here."

 - Make sure links are visually distinct by using underlining and other visual cues, so users can easily identify and navigate them.
 - Avoid generic link texts like "here", "click here", and "more-info" as they don't provide any useful information.
 - Aim for concise and descriptive link texts, ideally between 2-5 words, that convey the link's purpose.
 - Avoid jargon and abbreviations that users may not understand.
 - Focus on the destination, not the action. For example, "user behavior results", instead of "click here to read more".
 - Don’t repeat the same link text for different destinations.
 - Place links in a way that they make sense within the surrounding text. For example, "for more details, visit our events page" instead of "Click here for more".

```html
<a href="webinar-details-link">
  Get details about our upcoming webinar
</a>

```

```html

<a href="/blog-post-link">
   Read our latest blog post on web accessibility
</a>

```

[⬆ Back to Table of Contents](#table-of-contents)

## Video and audio accessible

The first thing you can do to make your videos more accessible is add captions to them, on the oder hand subtitles are important because people who may be don't understand the language or want to listen your content in quiet spaces can use this tool to improve their experience.

We can add caption as follow.

```html

<video
  width="400"
  height="300"
  controls
  src="https://cdn.freecodecamp.org/curriculum/labs/what-is-the-map-method-and-how-does-it-work.mp4"
>
  <track
    src="captions.vtt"
    kind="captions"
    srclang="en"
    label="English"
  />
</video>

<audio controls src="sample.mp3">
  <track
    src="captions.vtt"
    kind="captions"
    srclang="en"
    label="English"
  />
</audio>

```

The kind attribute is used to tell the track element how it should be used. Valid values for the kind attribute include captions, subtitles, chapters, and metadata.

The srclang attribute represents the language for the track content. The label attribute is a descriptive title for the text track that browsers use to identify and display it in the list of available text tracks.

Another important thing to consider is providing a transcript for your audio and video content. A transcript is a text version of all the spoken words in your audio or video. Unlike captions, transcripts don’t need to be synchronized with the media. Transcripts are useful for deaf people and those hard of hearing. They're also beneficial for people who prefer reading instead of watching or listening. Transcripts also make your content searchable, allowing users to quickly find specific parts of your audio or video. If you have a video or audio on a website, you can simply add the transcript below the audio or video:

```html

<audio controls>
  <source src="audio.mp3" />
  Your browser does not support the audio element.
</audio>

<!-- Transcript -->
<h3>Transcript</h3>
<p>
  [Speaker 1]: Welcome to the tutorial on making accessible content
</p>
<p>
  [Speaker 2]: Today, we'll cover captions, transcripts, and more.
</p>

<!-- Rest of transcript -->

```

If you're publishing videos on a video-sharing platform like YouTube or Vimeo, they have automatic captions and transcripts for videos. But if you're not satisfied, you can use services like veed.io, Rev, Amara, and Descript.

## Keyboard Navigation

If you want to control the natural tab behavie, you have to use the tabindex attribute.

```html

<element tabindex="number">Element Text</element>

```

```html

<button>First</button>
<div tabindex="1">Second</div>
<a href="#">Third</a>

```

tabindex="-1" makes an element focusable programmatically. This is useful for managing focus in elements that are not normally focusable, such as headings, containers, dialogs, or error messages:

```html
<p tabindex="-1">Sorry, there was an error with your submission.</p>
```

When the tabindex is greater than 0 it sets a custom tab order. So elements with lower positive values are focused first.

In this example, tabbing will focus the input with tabindex="1" first, then 2, then 3, regardless of their order in the HTML.

```html

<input tabindex="2">
<input tabindex="1">
<input tabindex="3">

```

accesskey is another attribute you can use to make your web project keyboard accessible. It allows you to define a key that focuses on or activates a particular element.

Here is an interactive example you can try out following the suggestions below (enable the interactive editor first):

 - accesskey="s" assigns the key S to the Save button. On most browsers, pressing ALT + S (on Windows) and CTRL + Option + S (on Mac) will activate this button.
 - accesskey="c" sets the key C to the Cancel button, allowing users to activate it using ALT + C (Windows) and CTRL + Option + C (Mac).
 - accesskey="h" assigns the key H to the Home link, allowing users to navigate to the homepage using ALT + H (Windows) and CTRL + Option + H (Mac).
Please note that the exact key combination to activate the accesskey might vary depending on the browser and operating system. It's typically ALT + Specified Key on Windows and CTRL + Option + Specified Key on Mac.

123
<button accesskey="s">Save</button>
<button accesskey="c">Cancel</button>
<a href="index.html" accesskey="h">Home</a>

```html

<button accesskey="s">Save</button>
<button accesskey="c">Cancel</button>
<a href="index.html" accesskey="h">Home</a>

```

## Summarize

To see the sumari of this content you click in the next link

[Summary accessibility](https://www.freecodecamp.org/learn/responsive-web-design-v9/review-html-accessibility/review-html-accessibility)

[⬆ Back to Table of Contents](#table-of-contents)

## HTML REVIEW

If you want a complete HTML review click in the next link

[Summarize of HTML](https://www.freecodecamp.org/learn/responsive-web-design-v9/review-html/review-html)

[⬆ Back to Table of Contents](#table-of-contents)
