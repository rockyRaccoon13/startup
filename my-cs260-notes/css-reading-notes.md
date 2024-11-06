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
change `box-sizing` from `content-box` to `border-box` to include padding and border (often easier because represents visual space (item + background) of element)



## [Selectors](https://github.com/webprogramming260/.github/blob/main/profile/css/selectors/selectors.md)

### element type selector

```css
body {
  font-family: sans-serif
}


* {
  font-family: sans-serif
}
```

## combinator

* descendant `body section`
* child `section > p`
* general sibling `div ~ p`
* adjacent sibling `div + p`

### Class selector

```css
.class {
  rules;
}

element.class {

}
```

### ID selector

```css
#uniqueID {
  rules
}
```

### attribute selector

``` css 
elemnt[atr = 'value'] {
  rules;
}

p[class = 'summary'] {
  rule;
}
p[href*="https://"] {}

```

### pseudo selector
```css
section:hover {
  rules;
}
```


## CSS declarations
rule declarations assign `property: value;`

| property | value | example | discussion | 
| --------- | -----| --------| ------- |
|background-color| color | `red` | fill background color |
| border | color width style |

## Responsive Design

Designed to respond to different viewports (phones desktops, etc) 

### Display
css display property 

```css
.class {
  display: value;
  /* values: none, block, inline, flex, grid 
      grid and flex require additional properties
    */
}
```

### Viewport meta tag
displays were auto scaling pages. to prevent auto scaling

```css
<meta name="viewport" content="width=device-width,initial-scale=1 />
```

### Float CSS property
 moves element right of container element and wraps inline elements around it

 ```css
 elementName {
    float: right; /* or left, inline-start/end, none*/
    padding: 3em;
    margin ...
    border...
 } 
 ```

### Media Queries

Media query tells us size and orientaion of device

if limited room because of portrait orientation 

```css
@media (orientation: portrait) {
  aside {
    display: none;
  }
}
```

GRID AND FLEX BOX are responsive designs that automatically respond to screen sizes to position and resize


## Grid

The grid display layout is useful when you want to display a group of child elements in a responsive grid. 


```css

.container {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  grid-auto-rows: 300px;
  grid-gap: 1em;
}

```


