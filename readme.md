# @suryadarsan/html-to-md

A lightweight package for converting HTML to Markdown, compatible with Vanilla JS and popular frameworks/libraries like Angular, React, and Node.js.

## Installation

You can install the package using npm:

```sh
npm install @suryadarsan/html-to-md
```

### Usage

#### Importing the Module
You can import the module in different ways depending on your environment:

#### Angular

##### Usage (for HTML string)
```ts
import { htmlToMd } from '@suryadarsan/html-to-md';

let md = htmlToMd(`<h1>Main Title</h1><p>This is a <strong>bold</strong> paragraph.</p>`);
console.log(md);
```

##### Usage (for HTML element)

###### HTML
```html
<main #convertMeToMD>

  ...

</main>
```

###### Typescript
```ts
import { htmlToMd } from '@suryadarsan/html-to-md';

...

@ViewChild('convertMeToMD')
convertMeToMD!: ElementRef;

...

let md = htmlToMd(this.convertMeToMD.nativeElement);
console.log(md);

```

#### React (ES Module)

###### Typescript
```ts
import { htmlToMd } from '@suryadarsan/html-to-md';

// HTML String
let md = htmlToMd(htmlString);
console.log(md);

// HTML Element
md = htmlToMd(document.querySelector('#someId'));
console.log(md);
...

#### CommonJS

```js
const { htmlToMd } = require('@suryadarsan/html-to-md');
```

#### jQuery
For use in the browser, include the UMD build:

##### Usage
```html
<script src="path/to/suryadarsan.htmlToMd.umd.js"></script>

 <script>
    var htmlString = `<h1>Main Title</h1>
    <p>
      For Link Example:
      <a href="https://www.example.com/my great page">link</a>
    </p>
    <h2>Heading 2</h1>`;
    $(function () {
      var md = suryadarsan.htmlToMd(htmlString);
      console.log(md);
    });
  </script>
```

#### UMD
For use in the browser, include the UMD build:

##### Usage
```html
<script src="path/to/suryadarsan.htmlToMd.umd.js"></script>

<script>
  var htmlString = `<h1>Main Title</h1>
<p>This is a <strong>bold</strong> paragraph.</p>

<ul>
  <li>Item 1</li>
  <li>Item 2</li>
</ul>

<h2>Heading 2</h1>
<ol>
  <li>Item 1</li>
  <li>Item 2 <a href="https://www.example.com/my great page">link</a></li>
</ol>

<b>Shortcut: </b> <code>Ctrl + A</code> 

<p>
  For Link Example:
  <a href="https://www.example.com/my great page">link</a>
</p>
<pre>console.log("Hello, world!");</pre>
`;
  console.log(suryadarsan.htmlToMd(htmlString));
</script>
```

#### Converting HTML to Markdown
You can convert an HTML string or an HTML element to Markdown using the `htmlToMd` function.

#### Example with HTML String

```js
const htmlString = '<h1>Main Title</h1><p>This is a <strong>bold</strong> paragraph.</p>';
const markdown = htmlToMd(htmlString);
console.log(markdown);
```

#### Example with HTML Element

```js
const element = document.getElementById('content');
const markdown = htmlToMd(element);
console.log(markdown);
```

#### API
`htmlToMd(input: string | HTMLElement): string`

Converts an HTML string or an HTML element to a Markdown string.

##### Parameters
- `input`: The HTML content to convert. It can be a `string` or an `HTMLElement`.

##### Returns
- A string containing the converted Markdown content.