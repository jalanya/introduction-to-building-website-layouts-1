# Introduction to Building Website Layouts

## Introduction to Building Website Layouts in HTML and CSS

### The Fluid Nature of the Web

The **Normal document flow** just means the normal way that the elements will display as they're written in the HTML file. Which, as you know, is from top to bottom -- as in "A block level element takes up the entire width of the page and the next element coming after it within the document, then gets displayed beneath it, etc... and so on and so forth"

So when someone says it, removes it from the normal document flow it's like...Hmm, Ok, think of it like this. Aside from inline elements, all the elements stack on top of each other, right? Well, instead of stacking on top of each other, I like to think of an HTML document as one big tetris game but from the bottom.

New elements are created below and come up from below and just like tetris blocks are always looking to go as far down as possible, elements do the same but UP. So elements are like these semantic tetris blocks that come in from the bottom and push their way up. They can only push as far as the element above them will allow.

Now, when you remove an element from the normal document flow, you're basically making a tetris. You're making that element's space that it's taking up across the page disappear. When that "space" disappears, the elements below it quickly move up to fill that space. So using one of the positioning schemes that "removes an element from the document flow" is basically like getting a tetris on that elements page space that it was taking up. It goes poof and the blocks(elements) below collapse upwards.

[HTML Document Flow](https://app.pluralsight.com/library/courses/html-document-flow-1837/) | [The Flow - The default behavior of a webpage](https://marksheet.io/css-the-flow.html) | [Quick Tip: Utilizing Normal Document Flow](https://webdesign.tutsplus.com/articles/quick-tip-utilizing-normal-document-flow--webdesign-8199)