# HTML Notes

[MDN DOCS](https://developer.mozilla.org/en-US/docs/Web/HTML)
[W3Schools](https://www.w3schools.com/html/default.asp)



## CodePen
CodePen is a coding sandbox
* immediately renders code
  * Can quickly see changes from code edits
* serves as a portfolio

## Hypertext Markup Language (HTML)
* Originally a publishing format for web documents
* Now a web page can be a web application
    * SPA or MPA (single page or multi p application)
* HTML is structure of web page
    * CSS will style web pages and JavaScript will make them interactive
 
### Example

```
<!DOCTYPE html>
<html lang="en">
  <body>
    <main>
      <h1>Hello world</h1>
      <p class="introduction">
        HTML welcomes you to the amazing world of
        <span class="topic">web programming</span>.
      </p>
      <p class="question">What will this mean to you?</p>
      <p class="assignment">Learn more <a href="instruction.html">here</a>.</p>
    </main>
  </body>
</html>
```
 
### Elements and Tags
`elements` are represented with enclosing `tags` 
  * elements enclose other elemnts or text
  * tags are delimted textual name i.e. `<tag>elements</tag>`

`html` is top level page structure
`head` contains metadata about the page and the page title element
`body` represents content structre
`main` is main content structure as opposed to headers, footers, asides, and navigation

### Attributes
elements may have attributes that describe details
`id` assigns unique id to identify a particular element instance
`class` used to group elements of common attributes

elements writen inside tagss with name='' (or "")
`<p id="hello" class="greeting">Hello world</p>`

### Hyperlinks
`a` - anchor elemnt -- element is a hyper link
`href` address of hyperlink reference
`<a href="https://byu.edu">Go to the Y</a>`

### DOCTYPE
**HTML defines a header `<!DOCTYPE html>`** that tells browser type and version of document
** ALWAYS INCLUDE THIS**

### Comments
`<!-- commented text -->`

### Special characters -- & escape characters
```
&	&amp;
<	&lt;
>	&gt;
"	&quot;
'	&apos;
😀	&#128512;
```

### index.html
the default web page served to browser from server -- when file not specified
'https://google.com' == 'https://google.com/index.html'
* index.html is commonly the main HTML file

### Rendering HTML
* you can open disk file in browser
* VS Code using ext Live Server to display HTML
* use a sandbox like HTML



## HTML Structure elements

common elements
`body`, `header`, `footer`, `main`, `section`, `aside`, `p`, `table`, `ol/ul`, `div`, and `span`

### Block and inline
Block element is a distinct block in the content structure
**inline element** meant to be inline in a block element

## HTML Input Elements
(https://learn.cs260.click/page/html/input/input_md)
(https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input)

### Form element

OG way before JS to get user input -- "name=value"

### input element

##HTML media elements
(https://learn.cs260.click/page/html/input/input_md)
### external media -- images, video, audio
### internal media-- drawings, animations-- SVG - scalable vector graphics, canvas
(https://developer.mozilla.org/en-US/docs/Web/SVG)






