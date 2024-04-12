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
  - 
