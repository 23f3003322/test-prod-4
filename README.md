# main goal
Publish a static page that converts input.md from attachments to HTML with marked, renders it inside #markdown-output, and loads highlight.js for code blocks.

## Project Summary
This project provides a small, static webpage that loads an embedded markdown source (representing an attachment named input.md) and renders it into HTML using the marked library. Syntax-highlighted code blocks are rendered using highlight.js. The page is designed to be deployed on GitHub Pages from a public repo.

## Setup (GitHub Pages)
1) Create a new repository on GitHub (or use an existing one).
2) Add the project files (index.html, README.md, LICENSE) to the repository.
3) Push the changes to GitHub.
4) In the repository settings, navigate to Pages.
5) Under Source, choose main branch and / (root). Save.
6) Access the site at https://<your-username>.github.io/<repo-name>/

Optional:
- Add a CNAME file if you want to use a custom domain.

## Usage
- Open the GitHub Pages URL in a browser.
- The page will render the content of input.md (embedded as a data URL in this static page) into HTML inside the element with id="markdown-output".
- Code blocks will be syntax-highlighted by highlight.js.

## Main Code Files and Their Purpose
- index.html
  - HTML scaffold, Bootstrap for basic styling, and inclusion of marked.js and highlight.js. The script fetches a data-URI-encoded input.md content (if available) and renders it inside #markdown-output using marked, with highlight.js for code blocks.
- README.md
  - This file documents the project, how to deploy on GitHub Pages, usage, and licensing.
- LICENSE
  - MIT license text.

## How the Markdown-to-HTML Rendering Works (high level)
- The page loads marked.js to parse Markdown into HTML.
- The page loads highlight.js to apply syntax highlighting to code blocks.
- JavaScript fetches a data URL representing input.md (if present) and passes the content to marked.parse. The resulting HTML is injected into the DOM at #markdown-output.

## License
MIT License

Copyright (c) 2025 Your Name

Permission is hereby granted, free of charge, to any person obtaining a copy
of the Software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies
of the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE USE OR OTHER DEALINGS IN THE
SOFTWARE.