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

#### ES Module (Angular / React)

```ts
import { htmlToMd } from '@suryadarsan/html-to-md';
```

#### CommonJS

```js
const { htmlToMd } = require('@suryadarsan/html-to-md');
```

#### UMD
For use in the browser, include the UMD build:

```html
<script src="path/to/suryadarsan.htmlToMd.umd.js"></script>
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