# Introduction to Building Website Layouts

## Introduction to Building Website Layouts in HTML and CSS

### The Fluid Nature of the Web

The **Normal document flow** just means the normal way that the elements will display as they're written in the HTML file. Which, as you know, is from top to bottom -- as in "A block level element takes up the entire width of the page and the next element coming after it within the document, then gets displayed beneath it, etc... and so on and so forth"

So when someone says it, removes it from the normal document flow it's like...Hmm, Ok, think of it like this. Aside from inline elements, all the elements stack on top of each other, right? Well, instead of stacking on top of each other, I like to think of an HTML document as one big tetris game but from the bottom.

New elements are created below and come up from below and just like tetris blocks are always looking to go as far down as possible, elements do the same but UP. So elements are like these semantic tetris blocks that come in from the bottom and push their way up. They can only push as far as the element above them will allow.

Now, when you remove an element from the normal document flow, you're basically making a tetris. You're making that element's space that it's taking up across the page disappear. When that "space" disappears, the elements below it quickly move up to fill that space. So using one of the positioning schemes that "removes an element from the document flow" is basically like getting a tetris on that elements page space that it was taking up. It goes poof and the blocks(elements) below collapse upwards.

[HTML Document Flow](https://app.pluralsight.com/library/courses/html-document-flow-1837/) | [The Flow - The default behavior of a webpage](https://marksheet.io/css-the-flow.html) | [Quick Tip: Utilizing Normal Document Flow](https://webdesign.tutsplus.com/articles/quick-tip-utilizing-normal-document-flow--webdesign-8199)


### Progressive Enhancement and Hierarchy

Progressive enhancement has been the hallmark of the responsible approach to standards-based web design. By beginning with a foundation of semantic, well-structured markup, styled with a layer of CSS, and DOM scripting via JavaScript added as needed, we can create compelling experiences in capable browsers, while ensuring universal access to the content beneath the design.

Stephen Hay reiterated the need for progressive enhancement as well, in his fantastic essay “[There is no Mobile Web](http://www.the-haystack.com/2011/01/07/there-is-no-mobile-web/)”.

**Book: A Book Apart - Responsive Web Design (2011)**

### HTML5 Sectioning Elements

In HTML, we have a group of elements that are referred to as sectioning elements, and there are many more added in HTML5 to make it easier to describe our content a more semantic way. So, sectioning elements are any of these elements that are intended to divide up content into these logical sections. Allows for us to build our outline in a semantic way and for styles to be applied to that grouped content. 

So, here's an example of some of our sectioning elements. This isn't the complete list, but these are some of the most common ones. So, we have our new HTML5 elements or newer, we have things like **`address, article, aside, header, footer, section, nav`, and prior versions of HTML, including HTML5, we also have `div`**, and while it's not really technically a sectioning element as we think of, the semantic elements added in HTML5, **`div`** is just a generic container for styling. So, you can think of it in the same category although it isn't technically a sectioning element. It achieves some of the same things. So, you've heard me refer to this word, semantic, a lot, and if you aren't familiar with semantic HTML, it just means taking the most meaningful and descriptive element as possible when you describe your content. 

[Flow content](https://www.w3.org/TR/2016/REC-html51-20161101/dom.html#kinds-of-content-flow-content) | [Sectioning content](https://www.w3.org/TR/2016/REC-html51-20161101/dom.html#kinds-of-content-sectioning-content) | [Heading content](https://www.w3.org/TR/2016/REC-html51-20161101/dom.html#kinds-of-content-heading-content)


### Adding External Fonts

[typekit](https://typekit.com) |
[Google Fonts](https://fonts.google.com/) |
[Adobe Creative](https://www.adobe.com/creativecloud.html)

### CSS Resets

[normalize.css](https://github.com/necolas/normalize.css)


### Typographic Scales and Vertical Rhythm

What is a Typographic Scale?

A way to set type size based on a ratio. Compared to setting type arbitrarily 
or based on "what looks good", using a typographic scale helps keep type 
size consistent and set in a way that is scientifically pleasing to the eye.

[Modular Scale](http://www.modularscale.com/) |
[CSS with vertical rhythm](https://drewish.com/tools/vertical-rhythm/)

### Understanding the Cascade: Source Order

Let's take a look at different ways in which styles can be applied to an element. The first way we can apply styles to an element is by **`authors`**. So, that's us as web designers and developers. If we write things like browser resets, like the normalize.css we pulled in, all of these are considered an author's style so created by the web person, web designer or developer. 

We also have **`users`** that can apply styles as well. And these sources will be coming from things like browser preferences. So, if they go in there and they change the default zoom or the default font that sites are using, the default font size, they can go into their settings for browsers and change all of these things themselves, which is going to generate an additional source of styles that are being applied. And there are also other ways that users can apply styles as well such as if they have accessibility issues or something of that nature, maybe they're using a program which is generating style sheets for them based on what preferences they have for their accessibility needs, or if they have poor vision and things of that nature. 

The last way styles can be applied is by **`user agents`**. So, these are things like generally browsers. So each different browser has its own set of default styles, which is why we see headings without any CSS being applied by us. There are default fonts already. There are default margins and paddings, and headings are bold, all of the things we see kind of reset to a baseline when we bring in a browser reset, like normalize.css, or something like that so we have those default browser styles to think about as well.

[Introducing the CSS Cascade](https://developer.mozilla.org/en-US/docs/Web/CSS/Cascade)

### Media Queries

```
@media screen and (min-width: 750px) {
  
  .main-navigation a:visited {
    color: red;
  }

}
```
Most mobile devices, or at least in portrait, are going to be smaller than about 650 pixels so we have a little bit of buffer there, and of course, we would want to test that assumption to ensure that, that is the case. **So, here it says media screen, and we're going to use minimum width as our condition so anything above 750 pixels, it's going to be served the style. So, `min-width: 750px`, and then we could add all our CSS we want to apply under these conditions inside.**

[Using media queries](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries) | [Targeting media features](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries#Targeting_media_features)

### Testing: Validation, Contrast, and Cross-browser

[W3C's validator Nu Checker](https://validator.w3.org/nu/) | [ Web Accessibility - Color contrast checker](https://webaim.org/resources/contrastchecker/)