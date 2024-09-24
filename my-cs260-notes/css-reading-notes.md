# Cascading Style Sheets (CSS)

## Introduction
[MDN CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)

CSS converts structure and content of HTML into virbrant, & responsive


CSS is primarily for defining `rulesets` or `rules`

rule is compromised of
 - `selector` -- selects elements
 - `declarations` 
    - `property` to style with `value`

example: 
```
p {
  font-family: sans-serif;
  font-size: 2em;
  color: navy;
  text-shadow: 3px 3px 1px #cccccc;
}
```

### Associating CSS with HTML

3 ways to asscoitate CSS with HTML

1. use `style` attribute of HTML element and expilicitly assign one or more declarations

```
<p style="color:green">CSS</p>
```

2. Define CSS Rules in HTML document
- `style` element should appear in `head` to apply rules to all elements 

```
<head>
  <style>
    p {
      color: green;
    }
  </style>
</head>
<body>
  <p>CSS</p>
</body>
```

3. use html `link` element to create hyperlink reference to file of CSS rules. link must be `head`. ** PREFERRED WAY**

```
<link rel="stylesheet" href="styles.css" />
```

styles.css
```
p {
  color: green;
}
```

### Precedence
Rules:
Element > html style element > external CSS file

nested: 
example : span inside p inside body
span rule has precedence



### Cascading Styles

Rules cascade dwon from highest nodes in DOM tree to lower nodes

** declaration property defined at lower level overides higher level declaration**

### selectors
| selector | meaning | example (css) | description|
|----------| --------|---------------|------------|

### The box model

CSS defines everything as boxes (and boxes within boxes)

display region is a box (element's are boxed)

content box
    - innermost - elements content
padding
    - inherit background color
border
    - properties like color, thickness, line style
margin 
    - external to styling
    - whitespace

Default width and height is **content box**
change `box-sizing` from `content-box` to `border-box` to include padding and border
