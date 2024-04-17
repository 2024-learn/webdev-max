# Web Development

- `<a href="https://xyz.com">this link</a>`: anchor element
- Anatomy of a vaild HTML document(page)

```html
<!DOCTYPE html> HTML version
<html>
  <head>
    page metadata
    <title> My Page </title>
  </head>
  <body>
    Page content
    <h1>Welcome!</h1>
  </body>
</html>
```

- comments in html: `<!-- abc-->`
- comments in CSS: `/* def */`

- How do browsers handle "whitespace" (line breaks and indentation)?
- How can you output special characters (e.g. "<") as text in HTML documents?
- How Browsers Handle Whitespace
  - In both HTML and CSS (and later also in "JavaScript"), as a developer, you typically try to format and structure code such that it is readable (for humans).
  - For example, the following two snippets contain the same code and hence would lead to the same result. The browser would understand both, but they are not equally readable / understandable for us humans:

  1. No formatting

  `<html><head><title>A test </title><style>h1{color:red}</style></head><body><h1>Hi there!</h1><p>This is some text...</p></body></html>`
  2. Formatting with line breaks and indentation (i.e. lots of "whitespace")

  ```html
  <html>
    <head>
      <title>A test </title>
      <style>
        h1 {
          color: red;
        }
      </style>
    </head>
    <body>
      <h1>Hi there!</h1>
      <p>This is some text...</p>
    </body>
  </html>
  ```

  - By default, the browser (typically - there are few exceptions, which we'll explore later) ignores line breaks and indentation in your HTML and CSS code. That's why, as a visitor of the site, you will see the same result for both snippets.
  - Since the result is the same, but we as a developer are a human, we typically go for the second approach - using lots of indentation and line breaks to structure and organize our code.
- How To Output Special Characters In HTML
  - When writing HTML code, characters like "<" and ">" obviously have a special meaning: They mark the beginning and ending of HTML tags.
  - But what if you would want to output the "<" and ">" characters or a complete HTML tag as text on your website? Like on this site here (yes, the site on which you currently are). You can read the code snippets above just fine - because they are output as plain text (they are NOT interpreted as HTML by the browser that loaded this page).
  - There are two main ways of achieving this:
  - You can use the special `<pre>...</pre>` tags (for "preformatted text") - these tags wrap any text (that may include HTML code) and "tell the browser" to output it as plain text (i.e. NOT interpret it as HTML code). When using `<pre>`, whitespace is also preserved and NOT ignored (as it normally would be)
  - Alternatively, if you simply want to output the "<" character (e.g. in some math formula that should be shown on your page), you can use some special "shortcuts" (so-called "HTML entities") in your HTML code:
  - E.g. if you write `&gt;` in your HTML code, the browser will output the ">" (greater than) symbol and `&lt;` => "<" (lower than)

- Creating lists:
  - ordered lists `<ol></ol>`
  - unordered lists: `<ul></ul>`

- Cascading, Inheritance and Specificity
  - Inheritance: (Selected) container rules apply to descendants
  - Cascading: Multiple rules can be applied to the same element
  - Specificity: more specific selector's rule wins over less specific selector

- Selectors and Combinators
  - Selectors:
    - Type: elementname
    - ID: #id - can only be used for one element
    - Group: elementname, elementname
    - Class: .class - like #id but can be used for multiple elements
  - Combinators: combination of different selectors
    - Descendant: e.g. li p - rules will apply to all p items with list item as ancestor
    - Child: e.g. h2 > p - only p items which are direct children of h2 would have the defined style

- Block (level) elements vs. Inline elements
  - A block element occupies the full width of the page and creates a new line. 
    - E.g. `<p>This is a block element</p>`
  - An inline element only occupies as much space as is needed for the content
    - E.g. `<p> This <a>link is an inline element</a> nested into a block element</p>`
    - common inline elements:
      - `<a>` : Link to other wesite/page of the current website
      - `<button>` : Clickable button to submit forms
      - `<img>` : Embed image into a HTML page
      - `<span>` : No-semantic inline container to mark-up text

- Box-shadow:
  - `box-shadow: offset on x-axis, offset on y, blur, rgba(0 0 0 1); 1 = opacity`
  - `box-shadow: 5px 5px 5px rgba(0 0 0 1);`

- __CSS selectors:__
- _Tag type selector_
  - CSS: `p { ... }`
  - Would select this HTML element for example: `<p>Some text...</p>`
  - This selector selects all HTML elements that are of this tag type

- _ID selector_
  - CSS: `#some-id { ... }`
  - Would select this HTML element for example: `<h1 id="some-id">...</h1>`
  - This selectors selects the element that has this ID on it (should only be once per page)

- _Class selector_
  - CSS: `.some-class { ... }`
  - Would select this HTML element for example: `<h1 class="some-class">...</h1>`
  - This selector selects all HTML elements that have this class on them

- _Attribute selector (new)_
  - CSS: `[src] { ... }`
  - Would select this HTML element for example: `<img src="...">`
  - This selector selects all elements that have this HTML attribute on them

- _Universal selector (new)_
  - CSS: * { ... }
  - Would select this HTML element for example: `<p>....</p><img ...>`
  - This selector selects ALL HTML elements (directly, not through inheritance but as if you would target them all individually)

- _Grouping selector / selector list_
  - CSS: `p, .some-class { ... }`
  - Would select this HTML element for example: `<p>...</p><h2 class="some-class">...</h2>`
  - This selector selects all elements that match the individual selectors in that list

- _Combined selector_
  - CSS: `p.some-class { ... }`
  - Would select this HTML element for example: `<p class="some-class">...</p>`
  - This selector selects all elements that meet both conditions (i.e. `"<p>"` elements with "some-class" class on it, in this example)

- _Pseudo selector_
  - CSS: `a:hover { ... }`
  - Would select this HTML element for example: `<a>...</a>` (when the user hovers over it)
  - This selector selects all elements that meet this "pseudo state" (i.e. all links that are hovered in this example)

- Instructing the browser
  - To open the link in the existing tab to `_self`:
    - `<a href="https://xyz.com" target="_self"> the MDN HTML element reference</a>.`
  - To open the link in a new tab, set the target to `_blank`:
    - `<a href="https://xyz.com" target="_blank"> the MDN HTML element reference</a>.`
