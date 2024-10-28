---
title: 'Semantic HTML5 Tags in 2024 for SEO'
description: Semantic components in your HTML layout help Search Engines better understand and rank your content, making them a fundamental part of SEO for your business. Whether you are working with freelance SEO marketing experts, using website builders for small businesses, or trying to design a website yourself, implementing these SEO-friendly elements can significantly improve your SEO optimisation for your website.
date: 2024-10-26T11:30:03+00:00
keywords: ["Semantic HTML5", "Technical SEO", "HTML5 SEO", "SEO for web developers", "HTML5 semantic elements", "Web accessibility and SEO", "HTML5 tags for SEO", "SEO-friendly HTML5", "SEO plugins for CMS", "Best HTML5 practices for SEO"]
tags: ["HTML5", "SEO Best Practices", "Semantic Elements"]
author: ["Balaji"]
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

Every year, almost 2.7 billion blog entries are written online, but almost <a href="https://ahrefs.com/blog/search-traffic-study/" title="Ahrefs study on search traffic" target="_blank" rel="noopener noreferrer">96% of them receive no traffic from Google's organic search results</a>. This lack of visibility often stems from inadequate application of technical SEO during the design and development of websites, which is crucial to improving your page rank.

## What is Semantic Markup in HTML ?
Unlike generic tags like `<div>` or `<span>`, semantic HTML5 elements such as `<header>`, `<article>`, and `<footer>` will help Search Engines better understand the content of a web page, which in turn improves indexing and visibility, making it easier for Search Engines to determine the hierarchy and importance of different sections.

   <figure>
      <img src="/img/Semantic_html_vs_nonSemantic_html.webp" alt="Comparison of Semantic and Non-Semantic HTML Elements" width="98%" height="80%"/>
      <figcaption>HTML5 Semantic help Search Engines with Better SEO.</figcaption>
   </figure> 

In this article, I will discuss on how <a style="box-shadow:none" href="#essential-html5-semantic-tags-to-use-in-websites" title="Usage of HTML5 semantic elements is an important factor for technical SEO">semantic HTML5 tags</a> enhance technical SEO and provide a list of essential tags you should always use when building or updating your site.

<div class="note">
<strong>Note:</strong>  </br>
Whether you are working with a white label SEO firm or simply looking to design your own website with a focus on SEO, Understanding Semantic HTML will be invaluable to your websites SEO.
</div>

## How Semantic HTML5 Tags Help SEO?

In January 2008, when HTML5 was released by the World Wide Web Consortium (<a href="https://www.w3.org" title="The World Wide Web Consortium (W3C)" target="_blank" rel="noopener noreferrer">W3C</a>). Its primary goal was to keep the web language easily readable by humans and interpretable by computers. As a result of this, new <a href="https://www.w3.org/wiki/HTML/New_HTML5_Elements" title="New Elements Introducted by W3C in HTML5" target="_blank" rel="noopener noreferrer">syntactic sugar HTML Elements</a> were introduced.<br>
This way, HTML semantic elements became the standard (natural) way of enabling Search Engine crawlers to understand what each section of a page is about. This allowed Search Engine algorithms to better analyze and process the content, rank (index) it, and render it in search results.

### Pros of Using HTML5 Semantic

#### 1. Make Websites Accessible for the Disabled:  
Semantic HTML helps users with <a href="https://www.michiganallianceforfamilies.org/cognitive-impairment/" target="_blank" rel="noopener noreferrer">cognitive disabilities</a> by providing clear, structured content that is easier to navigate and understand.  
Visually impaired users use <a href="https://www.afb.org/blindness-and-low-vision/using-technology/assistive-technology-products/screen-readers" title="Screen readers for the Blind" target="_blank" rel="noopener noreferrer">screen readers</a> to get a clear understanding of the context of each section of a page on a website.  Screen readers use web resources such as `Alt` text, `Aria` labels, color contrast, HTML structure (semantic tags) to announce them accordingly to the users.   
   ##### How to Measure Websites Accessibility Score ?     
   <a href="https://developer.chrome.com/docs/lighthouse/overview" target="_blank" rel="noopener noreferrer">Google Lighthouse</a> compares websites content against the Web Content Accessibility Guidelines and generates a score between 0 and 100.  

   <figure>
      <img src="/img/google_lighthouse_accessibility.webp" alt="Google Lighthouse Accessibility Score of Website" width="98%" height="80%"/>
      <figcaption>Lighthouse Accessibility Score for Frontend-Central Website</figcaption>
   </figure> 

   It will check for things like: 
   - HTML tags are semantically rich. 
   - Alternative Text is used in images.
   - ARIA landmarks are used. 
   - Buttons and Links are well described.   

#### 2. Web Standardization and Search Engine Optimization (SEO):  
HTML5 Semantic Elements were introduced to standardize the DOM structure on websites. This helps the Search Engines interpret the content and context of web pages better. 
Elements like `<header>`, `<nav>`, `<main>`, `<article>`, `<section>`, `<footer>` are semantic and help Search Engine crawlers understand the meaning and type of content inside them.

#### 3. Better Code Readability and Maintainability:   
Semantic HTML makes code more readable and understandable for developers, both for those who initially write it and for those who later maintain or update it.  

#### 4. Responsive Design:    
Developers can create flexible layouts using the viewport meta tag (`<meta name="viewport" content="width=device-width, initial-scale=1">`) that adapt seamlessly to various screen sizes and orientations, improving usability and accessibility on mobile devices.  

   ```html {linenos=table,hl_lines=["3-4"],linenostart=1}
   <head>
       <meta charset="UTF-8">
       <meta name="viewport" 
               content="width=device-width, initial-scale=1">
       <title>Your Website Title</title>
       <link rel="stylesheet" href="styles.css">
   </head>   
   ```

## Most Essential Semantic HTML5 Elements

There are more than 100 semantic elements declared and defined by the [WHATWG group](https://html.spec.whatwg.org/). I prefer, below are the **MUST** include HTML elements that will help Search Engines analyze and discover the contents of a website based on the enclosed HTML tag.

- `<header>`
- `<nav>`
- `<main>`
- `<article>`
- `<section>`
- `<footer>`  

### `<header>`: Header Element
The `<header>` element serves as the top section of a page or section, typically including the title, logo, navigation links, or other introductory content. Think of it as the "welcome area" for each part of your page.

   ```html
      <header>
         <h1>Title</h1>
         <nav>Home | About | Contact</nav>
      </header>
   ```

### `<nav>`: Navigation Element
The `<nav>` element defines a section of a webpage dedicated to navigation links, like menus or tables of contents, guiding users to different parts of the site or other documents.

   ```html
      <nav>
         <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Contact</a></li>
         </ul>
      </nav>
   ```

### `<main>`: Main Content Element
The `<main>` element defines the primary content of a page, focusing on the main topic or functionality. It excludes repetitive elements like headers, footers, or navigation.

   ```html
      <main>
         <h2>Article Title</h2>
         <p>This is the main content area of the page.</p>
      </main>
   ```

### `<article>`: Article Element
The `<article>` element defines a self-contained piece of content, such as a blog post, news article, or comment, that can be independently shared or repurposed.

   ```html
      <article>
         <h2>Blog Post Title</h2>
         <p>This post covers interesting facts about HTML elements.</p>
      </article>
   ```

### `<section>`: Section Element
The `<section>` element represents a standalone section of related content within a page, usually marked with a heading. It’s ideal for grouping content by topic or purpose.

   ```html
      <section>
         <h2>Features</h2>
         <p>Explore the unique features of our product.</p>
      </section>
   ```

### `<footer>`: Footer Element
The `<footer>` element serves as the closing section of a page or section, often containing metadata like author information, copyright, or links to related resources.

   ```html
      <footer>
         <p>&copy; 2023 My Company. All rights reserved.</p>
      </footer>
   ```

## Other Semantic HTML5 Elements to Know

Basically each HTML Element are segregated based on the categories (Sectioning content, heading content, phrasing content, embedded content, interactive content) they belong in different sections of the website.

<style>
  @media (min-width: 576px) {
   .Semantic-HTML-Tags-For-SEO {
      display: none;
   }
   }

   @media (min-width: 992px) {
   .Semantic-HTML-Tags-For-SEO {
      display: block;
   }
   }
</style>
   <div class="Semantic-HTML-Tags-For-SEO">   
   <svg xmlns="http://www.w3.org/2000/svg" viewBox="-250 -150 1000 288" width="1000" height="288">

   <style type="text/css">
      svg     { font: bold 18px sans-serif; text-anchor: middle; }
      svg ellipse { fill: #3c790a; stroke: #000000; opacity: 0.67; }
      svg text    { fill: #ffffff; pointer-events: none; }
      svg ellipse:hover { stroke-width: 5px; }
      svg ellipse:not(:hover) + foreignObject { display: none; }
      svg div { font: 14px sans-serif; }
      svg h1 { margin: 0 0 0.25em 0; padding: 0; font: 900 27px sans-serif; }
      svg ul { margin: 0; padding: 0 0 0 1em; }
      svg li { display: inline; margin: 0; padding: 0; line-height: 1.5; }
      svg li:not(:last-child):after { content: ', '; }
      svg span { font: italic 14px sans-serif; }
      svg code { font: 1em monospace; color: #CE3C05; }
      svg p { margin: 0.75em 0 0 0; padding: 0 0 0 1em; font: italic 14px sans-serif; }
   </style>
   <g class="a" transform="translate(2, -3)">
   <ellipse rx="244" ry="132"/>
   <foreignObject x="250" y="-150" width="500" height="288" transform="translate(-2, 3)">
      <div xmlns="http://www.w3.org/1999/xhtml">
      <h1>Flow content</h1>
      <ul>
      <li><code>a</code></li>
      <li><code>abbr</code></li>
      <li><code>address</code></li>
      <li><code>area</code></li>
      <li><code>article</code></li>
      <li><code>aside</code></li>
      <li><code>audio</code></li>
      <li><code>b</code></li>
      <li><code>bdi</code></li>
      <li><code>bdo</code></li>
      <li><code>blockquote</code></li>
      <li><code>br</code></li>
      <li><code>button</code></li>
      <li><code>canvas</code></li>
      <li><code>cite</code></li>
      <li><code>code</code></li>
      <li><code>data</code></li>
      <li><code>date</code></li>
      <li><code>datalist</code></li>
      <li><code>del</code></li>
      <li><code>details</code></li>
      <li><code>dfn</code></li>
      <li><code>dialog</code></li>
      <li><code>div</code></li>
      <li><code>dl</code></li>
      <li><code>em</code></li>
      <li><code>embed</code></li>
      <li><code>fieldset</code></li>
      <li><code>figure</code></li>
      <li><code>footer</code></li>
      <li><code>form</code></li>
      <li><code>h1</code></li>
      <li><code>h2</code></li>
      <li><code>h3</code></li>
      <li><code>h4</code></li>
      <li><code>h5</code></li>
      <li><code>h6</code></li>
      <li><code>header</code></li>
      <li><code>hgroup</code></li>
      <li><code>hr</code></li>
      <li><code>i</code></li>
      <li><code>iframe</code></li>
      <li><code>img</code></li>
      <li><code>input</code></li>
      <li><code>ins</code></li>
      <li><code>kbd</code></li>
      <li><code>keygen</code></li>
      <li><code>label</code></li>
      <li><code>link</code></li>
      <li><code>main</code></li>
      <li><code>map</code></li>
      <li><code>mark</code></li>
      <li><code>math</code></li>
      <li><code>menu</code></li>
      <li><code>meta</code></li>
      <li><code>meter</code></li>
      <li><code>nav</code></li>
      <li><code>noscript</code></li>
      <li><code>object</code></li>
      <li><code>ol</code></li>
      <li><code>output</code></li>
      <li><code>p</code></li>
      <li><code>picture</code></li>
      <li><code>pre</code></li>
      <li><code>progress</code></li>
      <li><code>q</code></li>
      <li><code>ruby</code></li>
      <li><code>s</code></li>
      <li><code>samp</code></li>
      <li><code>script</code></li>
      <li><code>search</code></li>
      <li><code>section</code></li>
      <li><code>select</code></li>
      <li><code>slot</code></li>
      <li><code>small</code></li>
      <li><code>span</code></li>
      <li><code>strong</code></li>
      <li><code>sub</code></li>
      <li><code>sup</code></li>
      <li><code>svg</code></li>
      <li><code>table</code></li>
      <li><code>template</code></li>
      <li><code>textarea</code></li>
      <li><code>time</code></li>
      <li><code>u</code></li>
      <li><code>ul</code></li>
      <li><code>var</code></li>
      <li><code>video</code></li>
      <li><code>wbr</code></li>     
      </ul>
      </div>
   </foreignObject>
   <text x="10" y="-94">Flow</text>
   </g>
         <g class="b" transform="translate(127, -48.5)">
         <ellipse rx="75" ry="42.5"/>
         <foreignObject x="250" y="-150" width="500" height="288" transform="translate(-127, 48.5)">
            <div xmlns="http://www.w3.org/1999/xhtml">
            <h1>Heading content</h1>
            <ul>
            <li><code>h1</code></li>
            <li><code>h2</code></li>
            <li><code>h3</code></li>
            <li><code>h4</code></li>
            <li><code>h5</code></li>
            <li><code>h6</code></li>
            <li><code>hgroup</code></li>
            </ul>
            </div>
         </foreignObject>
         <text x="2" y="6">Heading</text>
         </g>
         <g class="c" transform="translate(125, 42)">
         <ellipse rx="75" ry="42.5"/>
         <foreignObject x="250" y="-150" width="500" height="288" transform="translate(-125, -42)">
            <div xmlns="http://www.w3.org/1999/xhtml">
            <h1>Sectioning content</h1>
            <ul>
            <li><code>article</code></li>
            <li><code>aside</code></li>
            <li><code>nav</code></li>
            <li><code>section</code></li>
            </ul>
            </div>
         </foreignObject>
         <text x="1" y="5">Sectioning</text>
         </g>
         <g class="d" transform="translate(-113, 78)">
         <ellipse rx="117" ry="47" transform="rotate(-15)"/>
         <foreignObject x="250" y="-150" width="500" height="288" transform="translate(113, -78)">
            <div xmlns="http://www.w3.org/1999/xhtml">
            <h1>Metadata content</h1>
            <ul>
            <li><code>base</code></li>
            <li><code>link</code></li>
            <li><code>meta</code></li>
            <li><code>noscript</code></li>
            <li><code>script</code></li>
            <li><code>style</code></li>
            <li><code>template</code></li>
            <li><code>title</code></li>
            </ul>
            </div>
         </foreignObject>
         <text x="-4" y="8">Metadata</text>
         </g>
         <g class="e" transform="translate(-128, -34)">
         <ellipse rx="94" ry="51"/>
         <foreignObject x="250" y="-150" width="500" height="288" transform="translate(128, 34)">
            <div xmlns="http://www.w3.org/1999/xhtml">
            <h1>Interactive content</h1>
            <ul>
            <li><code>a</code></li>
            <li><code>audio</code></li>
            <li><code>button</code></li>
            <li><code>details</code></li>
            <li><code>embed</code></li>
            <li><code>iframe</code></li>
            <li><code>img</code></li>
            <li><code>input</code></li>
            <li><code>keygen</code></li>
            <li><code>label</code></li>
            <li><code>object</code></li>
            <li><code>select</code></li>
            <li><code>textarea</code></li>
            <li><code>video</code></li>
            </ul>
            </div>
         </foreignObject>
         <text x="-36" y="5">Interactive</text>
         </g>
         <g class="f" transform="translate(-40.5, -5)">
         <ellipse rx="76.5" ry="80"/>
         <foreignObject x="250" y="-150" width="500" height="288" transform="translate(40.5, 5)">
            <div xmlns="http://www.w3.org/1999/xhtml">
            <h1>Phrasing content</h1>
            <ul>
            <li><code>a</code></li>
            <li><code>abbr</code></li>
            <li><code>area</code></li>
            <li><code>audio</code></li>
            <li><code>b</code></li>
            <li><code>bdi</code></li>
            <li><code>bdo</code></li>
            <li><code>br</code></li>
            <li><code>button</code></li>
            <li><code>canvas</code></li>
            <li><code>cite</code></li>
            <li><code>code</code></li>
            <li><code>data</code></li>
            <li><code>date</code></li>
            <li><code>datalist</code></li>
            <li><code>del</code></li>
            <li><code>dfn</code></li>
            <li><code>em</code></li>
            <li><code>embed</code></li>
            <li><code>i</code></li>
            <li><code>iframe</code></li>
            <li><code>img</code></li>
            <li><code>input</code></li>
            <li><code>ins</code></li>
            <li><code>kbd</code></li>
            <li><code>keygen</code></li>
            <li><code>label</code></li>
            <li><code>link</code></li>
            <li><code>map</code></li>
            <li><code>mark</code></li>
            <li><code>math</code></li>
            <li><code>meta</code></li>
            <li><code>meter</code></li>
            <li><code>noscript</code></li>
            <li><code>object</code></li>
            <li><code>output</code></li>
            <li><code>picture</code></li>
            <li><code>progress</code></li>
            <li><code>q</code></li>
            <li><code>ruby</code></li>
            <li><code>s</code></li>
            <li><code>samp</code></li>
            <li><code>script</code></li>
            <li><code>select</code></li>
            <li><code>slot</code></li>
            <li><code>small</code></li>
            <li><code>span</code></li>
            <li><code>strong</code></li>
            <li><code>sub</code></li>
            <li><code>sup</code></li>
            <li><code>svg</code></li>
            <li><code>template</code></li>
            <li><code>textarea</code></li>
            <li><code>time</code></li>
            <li><code>u</code></li>
            <li><code>var</code></li>
            <li><code>video</code></li>
            <li><code>wbr</code></li>
            </ul>
            </div>
         </foreignObject>
         <text x="0" y="-39.5">Phrasing</text>
         </g>
         <g class="g" transform="translate(-42, -7)">
         <ellipse rx="68" ry="22.5"/>
         <foreignObject x="250" y="-150" width="500" height="288" transform="translate(42, 7)">
            <div xmlns="http://www.w3.org/1999/xhtml">
            <h1>Embedded content</h1>
            <ul>
            <li><code>audio</code></li>
            <li><code>canvas</code></li>
            <li><code>embed</code></li>
            <li><code>iframe</code></li>
            <li><code>img</code></li>
            <li><code>math</code></li>
            <li><code>object</code></li>
            <li><code>picture</code></li>
            <li><code>svg</code></li>
            <li><code>video</code></li>
            </ul>
            </div>
         </foreignObject>
         <text x="0" y="7">Embedded</text>
         </g>
      </svg>
   </div>

<br>

<div class="did-you-know" >
<h3>Did You Know</h3>
<ol>
<li><strong>Negative Impact on SEO</strong>
 <p>Ignoring HTML semantic elements will cause Search Engine crawlers to see the page as only plain text, links, and images. They won't understand the content and context within the page, leading them to conclude it is low-quality content, which may result in a lower ranking in search results.</p></li>

<li><strong>Case Study on Visually Impaired Users</strong>
 <p>In a study of 100 visually impaired users, it was found that they lose an average of 30.4% of their time due to <a href="https://www.researchgate.net/publication/220302591_What_Frustrates_Screen_Reader_Users_on_the_Web_A_Study_of_100_Blind_Users" title="Ignoring HTML Semantic Elements Will Frustrate Screen Reader Users" target="_blank" rel="noopener noreferrer">frustrating situations with screen readers</a>. This makes it harder for them to interpret content and navigate to other pages or sections on the web.</p></li>

<li><strong>Code Maintenance Challenges</strong>  
 <p>A website full of non-semantic HTML tags like <code>&lt;div&gt;</code>, <code>&lt;span&gt;</code>, and <code>&lt;p&gt;</code> will make the code harder to maintain and update over time for developers.</p></li>
</ol>
</div>


## Conclusion

Whether you are building the site yourself or hiring an experienced web agency, make sure to include the necessary semantic HTML elements in your website. This will ensure that your website is SEO-friendly and ranks higher in search results, ultimately driving more traffic to your site.