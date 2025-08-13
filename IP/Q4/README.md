**4. Explain three ways of inserting a CSS to a document using example?**

There are three ways to insert CSS into a document:

**1. Inline CSS**
In this method, CSS is applied directly within an HTML tag using the style attribute.
Example:

`<h1 style="color: blue; font-size: 20px;">This is a heading</h1>`

**2. Internal CSS**
In this method, CSS is written inside the `<style>` tag within the `<head>` section of the HTML document.
Example:

`<html>`
`<head>`
`<style>`
`h1 {`
`  color: green;`
`  font-size: 25px;`
`}`
`</style>`
`</head>`
`<body>`
`<h1>This is a heading</h1>`
`</body>`
`</html>`

**3. External CSS**
In this method, CSS is written in a separate .css file and linked to the HTML document using the `<link>` tag.

Example (HTML file):
`<html>`
`<head>`
`<link rel="stylesheet" type="text/css" href="style.css">`
`</head>`
`<body>`
`<h1>This is a heading</h1>`
`</body>`
`</html>`

Example (style.css file):
`h1 {`
`  color: red;`
`  font-size: 30px;`
`}`
