# CodeSquad's HTML best practices

### Use the HTML5 doctype declaration at top of html page `<!DOCTYPE html>`
There are many different versions of HTML that can be run in modern browsers such as HTML5, HTML 4.01 Strict, XHTML 1.0 Frameset, and others.  A browser can get confused about how to interpret your html in some cases.  CodeSquad standardizes on HTML5 so to avoid unexpected behavior you should put the HTML5 doctype declaration, `<!DOCTYPE html>` at the beginning of your HTML files.


#### Bad
Missing entirely
```html
<html>
  <body>
   ...
```

Don't use in middle or end of page.
```html
<html>
  <!DOCTYPE html>
  <body>
   ...
```

#### Good
Always use at top of page.
```html
<!DOCTYPE html>
<html>
  <body>
   ...
```


### Always use `<html>` and `<body>` tags when making a web page.
The `<html>` and `<body>` elements are automatically added by most browsers but you should explicitly write them in your code for every web page so that your code is understood to be a full web page and not a template or HTML fragment.  This is important as we start using javascript frameworks that support templating.  There are also useful attributes that these two elements can be assigned such as `<html lang="en">` which specifies the language is English on the page.


#### Bad
Missing `<html>` tag.
```html
<body>
  <h1>My page</h1>
  ...
</body>
```

Missing `<body>` tag.
```html
<html>
  <h1>My page</h1>
  ...
</html>
```

Missing `<html>` and `<body>` tags.
```html
<h1>My page</h1>
...
```

#### Good
```html
<html>
  <body>
    <h1>My page</h1>
    ...
  </body>
</html>
```

### Always use lowercase letters for tags.
Lowercase letters are easier to type, easier on the eyes to read, and a well established convention for writing tags used by web developers across the globe.

#### Bad
All capitals.
```html
<H1>My title is <STRONG>GREAT</STRONG></H1>
```

#### Really Bad
Mixed case.
```html
<h1>My title is <sTrong>GREAT</Strong></H1>
```
#### Good
```html
<h1>My title is <strong>GREAT</strong></h1>
```

### Always use double quotes around attribute values.
HTML does not require quotes around attribute values when the value has no spaces but leaving them off is a common cause for errors and makes for less readable code.  

#### Bad
Missing quotes
```
<a href=http://google.com>Google</a>
```
#### Good
```
<a href="http://google.com">Google</a>
```

### Never use spaces between the equals and the attribute's name and value
Using spaces between the equals and the attribute's name and value makes it harder to see that the value and the name are together.

### Bad
```
<a href = "http://google.com">Google</a>
```
### Really Bad
```
<a href        =           "http://google.com">Google</a>
```
### Good
```
<a href="http://google.com">Google</a>
```

### Use indentation and line breaks when showing nested elements within a parent element.
Use indentation to make it clear to other developers what block elements are contained within other elements and make it easier to scan those elements. However, it usually makes sense to leave inline elements within the flow of the text.

#### Bad
Not clear which elements are nested and which are sibling elements.
```html
<div>
<h1>Title</h1>
<p>Interesting Content</p>
</div>
```
Too hard to scan what elements are in the `<div>`
```html
<div><h1>Title</h1><p>Interesting Content</p><p>and more</p></div>
```

#### Good
```html
<div>
  <h1>Title</h1>
  <p>Interesting Content</p>
  <p>and more</p>
</div>
```
```html
<div>
  <h1>Title</h1>
  <p>This <em>inline block</em> is nested but is okay not to indent.</p>
  <p>and more</p>
</div>
```
