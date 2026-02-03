## Table of Contents

- [HTML the basics](#html-the-basics)
- [Basic tags](#basic-tags)
  - [Headings h1 - h6](#headings-h1---h6)
  - [Emphasis em element](#emphasis-em-element)
  - [Strong element](#strong-importance-element)
  - [Figure and figcaption](#figure-and-figcaption-element)
- [Attributes](#attributes)
- [HTML Boiling plate](#html-boiling-plate)
  - [Link element](#link-element)
- [HTML Fundamentals](#html-fundamentals)
  - [Div element](#div-element)
  - [ID](#ids-and-classes)
  - [Classes](#classes)
  - [HTML entities](#html-entities)
- [How HTML affects SEO](#how-html-affects-seo)
  - [Meta Description](#rol-of-the-meta-description)
  - [Open Graph tags](#role-of-open-graph-tags)
- [Audio and video elements](#role-of-the-audio-and-video-elements)
- [Working with Images and SVGs](#working-with-images-and-svgs)
  - [Optimize images SVG](#ways-to-optimize-format-license)
  - [Images license](#image-license)
  - [SVGs when use them](#svg-when-use-them)
- [Working with Iframe element](#working-with-iframe-element)
  - [Replaced elements](#replaced-elements)
  - [Iframe](#iframe)
  - [How embed videos onto your page](#how-do-you-embed-videos-onto-your-page-using-the-iframe-element)
- [Working with links](#working-with-links)
  - [What are the different target attribute types](#what-are-the-different-target-attribute-types-and-how-do-they-work)
  - [Absolute and relative paths](#absolute-and-relative-paths)
  - [Difference between slashes dot double dot in path syntax](difference-between-slashes-dot-double-dot-in-path-syntax)
  - [Link states](#link-states)
- [Basic HTML summary](#basic-html-summary)

# HTML the basics

**HTML** stands for "*Hyper Text Markup Language*". It's the code that defines the structure and content of a webpage.

[⬆ Back to Table of Contents](#table-of-contents)

## Basic tags

### Headings H1 - H6

We have the title tag, which can go from `<h1>` to `<h6>`. Here there are some basic tags also called "***elements***".

```html
<h>
<p>
<img src="" alt=""/>
<a href=""></a>
<input/>
```

### Emphasis (em) Element

This is used to place emphasis on a piece of text.

```html

<p>Cats <em>love</em> lasagna.</p>  

```

### Strong importance element

This element is used to place strong emphasis on text to indicate a sense of urgency and seriousness.

```html

<p>
  <strong>Important:</strong> Before proceeding, make sure to wear your safety goggles. 
</p>

```

### Figure and Figcaption element

The figure element is used to group content like images and diagrams. The figcaption element is used to represent a caption for that content inside the figure element.

```html

<figure>
  <img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/cats.jpg" alt="Two tabby kittens sleeping together on a couch.">
  <figcaption>Cats <strong>hate</strong> other cats.</figcaption>  
</figure>

```

[⬆ Back to Table of Contents](#table-of-contents)

## Attributes

An attribute is a value placed inside the opening tag of an HTML element. Attributes provide additional information about the element or specify how the element should behave.

`<element attribute="value"></element>`

[⬆ Back to Table of Contents](#table-of-contents)

## HTML boiling plate

### Link element

This element is used to link external resources like stylesheets and site icons.

`<link rel="stylesheet" href="./styles.css" />`

The rel attribute is used to specify the relationship between the linked resource and the HTML document, in this case, we're saying that this resource is a stylesheet.

We can use multiples link tags in the same file this is correct if you want to for example, use icons, stylesheet and even a favicon. 

```html

<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link
  href="https://fonts.googleapis.com/css2?family=Playwrite+CU:wght@100..400&display=swap"
  rel="stylesheet"
/>

```

In the example above we can see the value "*preconnect*", for the rel attribute, this tells the browser to create an early connection to the value specified in the href attribute. This is done to speed up loading times for these external resources.  

[⬆ Back to Table of Contents](#table-of-contents)

## HTML Fundamentals

### Div element

The div element works by grouping HTML elements that share similar CSS styles, this element is used just for styling purposes, remember that if you want to separate content based on its content, you should use the semantic tag **section**.

### ID's and classes

The ID attribute adds a unique identifier to an HTML element. Remember that you cannot repeat this value and it has to be unique and with no spaces.

### Classes

In contrast to the id attribute the class attribute value does not need to be unique and can contain spaces.

You can add multiple classes to an element by separating the names by a space. Here is an example.

```html

<div class="box red-box"></div>

```

[⬆ Back to Table of Contents](#table-of-contents)

### HTML Entities

An HTML entity, or character reference, is a set of characters used to represent a reserved character in HTML.

```html

<p>This is an &lt;img /&gt; element</p>

```

The previous code works in HTML you are going to see in the screem something like this.

```html

This is an <img /> element.

```

[⬆ Back to Table of Contents](#table-of-contents)

## How HTML affects SEO

### Rol of the Meta description

SEO or (Search Engine Optimization) is a practice that optimizes web pages so they become more visible and rank higher on search engines.

One of these practices is using the meta elemente **description** where we are going to put a short description of our web page. 

```html
<meta
  name="description"
  content="Discover expert tips and techniques for gardening in small spaces, choosing the right plants, and maintaining a thriving garden."
/>

```

By setting the name attribute to **description**, it ensures that browsers, correctly interpret this metadata.

In the content attribute you should add a short and concise summary of your page. Remember that this description can appear in below the link in search engines.

[⬆ Back to Table of Contents](#table-of-contents)

## Role of Open graph tags

The open graph protocol enables you to control how your website's content appears across various social media platforms. By setting these open graph properties, you can entice users to want to click and engage with your content.

The first important OG property to include would be the tittle. 

```html

<meta content="freeCodeCamp.org" property="og:title" />

```

Other important OG property is the type property.

```html

<meta property="og:type" content="website" />

```

The image OG propertie is also very important.

```html

<meta
  content="https://cdn.freecodecamp.org/platform/universal/fcc_meta_1920X1080-indigo.png"
  property="og:image"
/>

```

"use images that are at least 1200 by 630 pixels for the best display on high resolution devices. At the minimum, you should use images that are 600 by 315 pixels to display link page posts with larger images."

The fourth important OG property would be the url. Here is an example of setting the OG url for the freeCodeCamp homepage:

```html

<meta property="og:url" content="https://www.freecodecamp.org" />

```
[⬆ Back to Table of Contents](#table-of-contents)

## Role of the audio and video elements

### Audio

You can play audio in format mp3, wav, ogg. Use this tag as follow.

```html

<audio src="https://cdn.freecodecamp.org/curriculum/js-music-player/cruising-for-a-musing.mp3"
loop
controls
muted
> 

</audio>

```

When you add the propertie controls, the display shows a control as the common media players, without this text you cannot see nothing in the screem.

There are any other kind of attributes to enhance the audio tag. For example the loop attribute which makes the audio replay continuosly.

You can also use the muted attribute which start the audio in mute.

If you don't know what kind of audio the browsers are going to support, you can set a list of different types of audio and the browser is going to select the one which it understands. 

```html

<audio controls>
  <source src="audio.ogg" type="audio/ogg" />
  <source src="audio.wav" type="audio/wav" />
  <source src="audio.mp3" type="audio/mpeg" />
</audio>

```

### Video

The same attributes that we've seen before, works to the video elements. Just two attributes more.

The first one is the "autoplay" attribute which make the video plays automatically. And the width attribute which allows set a specific size to the video. 

```html

<video
  src="https://archive.org/download/BigBuckBunny_124/Content/big_buck_bunny_720p_surround.mp4"
  loop
  controls
  muted
  poster="https://peach.blender.org/wp-content/uploads/title_anouncement.jpg?x11217"
  width="400"
></video>

```

You can add a lot of sources if you don't know what kind of video supports the browser as the same way we do with the audio elements.

Is neccesary tell to the browser what type of video we are sending. In this case we use "type" to this purpose. 

Finally the poster attribute is only for video elements, and it shows a poster while the video is being downloading.

```html

<video
  loop
  autoplay
  controls
  muted
  width="400"
  poster="https://peach.blender.org/wp-content/uploads/title_anouncement.jpg?x11217"
>
  <source src="src-url-goes-here" type="video-type-goes-here" />
  <source src="https://cdn.freecodecamp.org/curriculum/labs/mapmethod.webm" type="video/webm"/>
</video>

```

[⬆ Back to Table of Contents](#table-of-contents)

## Working with images and SVGs

## Ways to optimize Format, license

There are three tools to consider when using media, such as images, on your web pages: the size, the format and the compression.

### Format

Two of the most common file formats are PNG and JPG, but these are no longer the most ideal formats for serving images. You should consider using a more optimized format, like WEBP or AVIF. 

### Image License

There are some pages which allow you download free imagenes, such as.

- pixabay

- unsplash

[⬆ Back to Table of Contents](#table-of-contents)

## SVGs when use them

First of all, we need to understand that normal images like PNG or JPG are classified as **raster formats** this means that they are pixel-based, that's why if you want to make a PNG or JPG image larger, you may have seen that it becomes pixelated or blurry.

Now let's talk about **SVG** images which stands for *scalable vector graphic*. A vector graphic tracks data based on paths and equations to plot points, lines, and curves. What this really means is that a vector graphic, like an SVG, can be scaled to any size without impacting the quality.

SVGs specifically have the added benefit of storing data in XML. This means you can use them directly in your code as raw HTML with the svg element. It also means you can programmatically change the color of the image.

```html

<svg width="100" height="100" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
  <circle cx="50" cy="50" r="45" stroke="black" stroke-width="4" fill="yellow" />
  <circle cx="35" cy="40" r="5" fill="black" />
  <circle cx="65" cy="40" r="5" fill="black" />
  <path d="M35 65 Q50 80 65 65" stroke="black" stroke-width="4" fill="transparent" />
</svg>

<!-- Star Icon -->
<svg width="50" height="50" viewBox="0 0 24 24" fill="gold" xmlns="http://www.w3.org/2000/svg">
  <path d="M12 2L14.9 8.6L22 9.3L17 14.1L18.3 21.2L12 17.8L5.7 21.2L7 14.1L2 9.3L9.1 8.6L12 2Z"/>
</svg>

<!-- Heart Icon -->
<svg width="50" height="50" viewBox="0 0 24 24" fill="crimson" xmlns="http://www.w3.org/2000/svg">
  <path d="M12 21.35L10.55 20.03C5.4 15.36 2 12.28 2 8.5C2 6 4 4 6.5 4C8 4 9.5 4.8 10.5 6.09C11.5 4.8 13 4 14.5 4C17 4 19 6 19 8.5C19 12.28 15.6 15.36 10.45 20.04L12 21.35Z"/>
</svg>

<!-- Checkmark Icon -->
<svg width="50" height="50" viewBox="0 0 24 24" fill="green" xmlns="http://www.w3.org/2000/svg">
  <path d="M20.29 5.71L9 17L3.71 11.71L5.12 10.29L9 14.17L18.88 4.29L20.29 5.71Z"/>
</svg>

```

The svg element is the container for the whole drawing. It sets up the space where all the shapes appear. Everything you wnat to draw with SVG, such as circles, lines, or paths, goes inside the svg element.

The circle elements are the circles that compose the face. And the path element is to draw the smile of the face.

When you use SVG? A great approach is for icons or logos. That's why you can scale to any size in a responsive web. 

One very common pages to find incons and logos is.

 - Font Awesome

[⬆ Back to Table of Contents](#table-of-contents)

## Working with Iframe element

## Replaced elements

First we have to understand what is a replaced element. This kind of element is an elements whose content is determined by an external resource rather than by CSS itself. CSS cannot directly modify the content of that element just things like position of the element or its layout and maybe apply filters but is imposible modify the image itself, the same thing happends with videos.

```html

<img src="example-img-url" alt="Descriptive text goes here">

```

In the previous example we can see that this is a replaced element because the source is a external link, so you can change the position, maybe the size but you cannot modify the image itself.

### Iframe

In this case we are going to talking about a more robust example of this kind of element which is the iframe element, which embeds an external site on your web page.

For example we can see youtube videos through an Iframe as follow.

```html

<iframe width="400" height="200" src="https://www.youtube.com/embed/u43gJJrVa1I?si=BoDW_puFsy8OEr_Z" title="Professional Cloud Architect Certification Course – Pass the Exam! (YouTube video)" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

```

The Iframe just doesn't work to show videos, we can also use this tag, to show maps and any other pages into ours.

```html
<iframe
  title="Map of the Royal Observatory, Greenwich, London"
  width="300"
  height="200"
  src="https://www.openstreetmap.org/export/embed.html?bbox=-0.004017949104309083%2C51.47612752641776%2C0.00030577182769775396%2C51.478569861898606&amp;layer=mapnik">
</iframe>

```

### How do you embed videos onto your page using the iframe element?

Here there is an example about how show a video into your page.

```html

<iframe
  width="400"
  height="400"
  src="https://www.youtube.com/embed/PkZNo7MFNFg?si=-UBVIUNM3csdeiWF"
  title="Learn JavaScript - Full Course for Beginners (YouTube video)"
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
  referrerpolicy="strict-origin-when-cross-origin"
  allowfullscreen
></iframe>

```

So let's to give the meaning of each attribute show before.

 - src : Specifies the URL of the page you wanto to embed.

 - width : Is just to set the width of the page
 - height : In the same way as widht, its purpose is the same
 - title : Is uses for accessibility
 - allow accelerometer : This allow the sensors detect things like device tilting and rotation.
 - allow autoplay: This attribute is to play automatically play the video.
 - allow clipboard-write: It means that you can copy or paste or this kind of actions in the embed element.
 - allow encrypted-media: Allow the use of encrypted media extensions to protect the video
 - allow gyroscope: Grant access to the device’s motion and orientation sensors
 - allow picture-in-picture:
 - allow web-share: Allow sharing the iframe content through the device's native share dialogs. 
 -referrerpolicy: Is the rule that determines how much detail you share when your page connects to another page
 -allowfullscreen: Allow the user use the full screem to see the element embed

 If you want to use the iframe tag to show an HTML page you have to use the *srcdoc* instead of *src*.

[⬆ Back to Table of Contents](#table-of-contents)

## Working with links

### What Are the Different Target Attribute Types, and How Do They Work?

There are four important possible values for this attribute. 

#### _self

```html

<a href="https://freecodecamp.org" target="_blank">Visit freeCodeCamp</a>

```

This open the new window in the same tab or window.

#### _blank

Open the link in a new browsing context, or in a new browser tab.

#### _parent

This open the new window in a parent of the current context, for example, of you have an Iframe, and this page has a link who is configurated as a _parent, the new window will be open in your current page not in the embedded frame.

#### _top

This target works similar to the parent target, but insted open the link in the parent context, _top, open the link in the top-most browsing context, this means in the parent of the parent and so on. 

[⬆ Back to Table of Contents](#table-of-contents)

## Absolute and relative paths

#### Absoulte path

This kind o path includes even the protocol.

```html

<a href="https://design-style-guide.freecodecamp.org/img/fcc_secondary_small.svg">
  View fCC Logo
</a>

```

If the file is in your machine it will look like.

```html
<p>
  Read more on the
  <a
    href="/Users/user/Desktop/fCC/script-code/absolute-vs-relative-paths/pages/about.html"
    >About Page</a
    >
</p>

```

#### Relative path

The relative path specifies the location of a file relative to the directory of the current file.

```html

<p>
  Read more on the
  <a href="about.html">About Page</a>
</p>

```

[⬆ Back to Table of Contents](#table-of-contents)

## Difference between slashes dot double dot in path syntax

### slash \ /

This is usually known as "path separator". For example.

***naomis/files/*** - points to a files directory in the naomis directory.

### point .

A single dot points to the current directory, and two dots point to the parent directory. You will typically see a single dot use to ensure that the path is recognized as a relative path.

[⬆ Back to Table of Contents](#table-of-contents)

## Link states

There are different link states, for example.

 - :link => When the links hasn't been visited yet
 - :visited => When the lik has been already visited
 - :hover => When you pass the cursor over the link
 - :focus => When you have actived the link.
 - :active => When you click on the link.

 When you want to style your link, you have to follow the next order.

 link - visited - hover - active

[⬆ Back to Table of Contents](#table-of-contents)

## Basic HTML summary

In the next link you are going to find a summary of basic html

[Basci HTML summary](https://www.freecodecamp.org/learn/responsive-web-design-v9/review-basic-html/basic-html-review)


- **ROLE OF HTML :** Stands for *Hyper Text Markup Language* and represent the content and structure of the web page. 

- **HTML ELEMENTS :** Elements are the building blocks for an HTML document. They represents headings, paragraphs, links, images and more. Most elements consist of an opening tag and a closing tag. But there are some elements which just have the start tag, for example. 

  - &lt;img>
  - &lt;br>
  - &lt;hr>
  - &lt;link>
  - &lt;meta>
  - &lt;source>

- **ATTRIBUTES :** An attribute is a value placed inside the opening tag of an HTML element. Attributes provide additinal information about the element or specify how the element should behave. There is also something called the boolean attribute, this kind of attribute can be present or absent, if present the value will be true otherwise it will be false
Some examples of boolean attributes are:
  - disabled
  - checked
  - readonly
  - required
  - autofocus
  - multiple
  - selected
  - hidden

- **COMMON HTML ELEMENTS** : There are a lot of html elements but I'm going to put here just the most unknown for me.

  - **Emphasis (em) Element** : This is used to place emphasis on a piece of text.

  - **Strong importance Element** : This element is used to place strong emphasis on text to indicate a sense of urgency and seriousness.

  - **Figure and figcaprion Element** : The figure caption element is used to group content like images and diagrams. The figcaption element is used to represent a caption for that content inside the figure element.

- **ID'S AND GROUPING** : ID is a unique identifier and can also be used once per html document. This ID's cannot have spaces into the name, if you wanto to separate words you have to use dashes. *(id="first-name")*.

  **Classes** are different, they can be used more than once through the document, and is used to group elements for styling o behavior.

- **ENTITIES** : The entities or character reference are a set ot characters used to represent reserved values in HTML, for example.

  - The ampersan &amp;
  - Less than &lt;
  - Greather than &gt;

- **LINK ELEMENT** : The link element is used to link to external resources like stylesheets or icons.

  - The **rel** attribute represents the relationship between the linked resource and the document.
  - The **href** attribute represents the exact ubication of the resource.

- **SCRIPT** : The script tag is used to link with **JS** files the **src** attribute is used to give the exact direction or ubication of the file.

- **HTML BOILERPLATE** : This is the structure and essential elements that every HTML document need.

  ```html

  <!DOCTYPE html>
  <html lang="en">
    <head>
      <meta charset="utf-8"/>
      <title>Page name</title>
      <link rel="stylesheet" href="#"/>  
    </head>  
    <body>
      <!-- All the content of the page -->
    </body>
  </html>  
  
  ```

- **SEO and social sharing** : SEO which stands for *Search engine optimization* is a group of practices that make your web page more visible and rank higher on search engines. Some useful tags to improve the SEO of your page can be:
  
  - **Meta(Description)**: This is used to provide a short description for the web and impacting the SEO.
  - **Open Graph Tags** : The open graph protocol enables you control how your website's content appear across various social media plataforms, such as facebook, linkendln, and many more.
  You can set these properties through a collection of **meta** elements inside your HTML head section. 

- **Media elements and optimization** : Replaced elements are resources determined by an external resource rather than CSS itself. An example would be the **iframe** element which stands for, **inline frame**, you cannot modidy the content of this kind of elements with CSS, because the original content comes to your page from other source and external one. 

- **Media** : There are three principal tools to consider when using media, they are, size, format and compression. 
You should use **WEBP** or **AVIF** instead PNG or JPG when use images on your page. Remember using **SVG's** formats to your logos or icons.

- **Multimedia integration**: The **audio** and **video** elements, allow you to add sound and video content to your web page.

  - **audio** : The audio element can be composed by various sources if maybe one of them don't work and also has some boolean attributes to set its behave.

  ```html
  <audio
    controls
    loop
    mute
  >
    <source src="audio.ogg" type="audio/ogg" />
    <source src="audio.wav" type="audio/wav" />
    <source src="audio.mp3" type="audio/mpeg" />
  </audio>
  ```
- **Target value** : This element define the place where the links will be open. There are four principal targets.

  - **_self** : Thi is the default value, this opens the link in the current browsing context.

  - **_blank** : This opens the link in a new browser context.

  - **_parent** : This opens the link in the parent browser context, it means that if the link is in a Iframe context, the link will be open in your browser context.

  - **_top** : This opens the link in the top-most browsing context. 


[⬆ Back to Table of Contents](#table-of-contents)
