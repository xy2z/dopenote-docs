---
description: 'Code standard, etc.'
---

# Contributing

_Dopenote is build in the PHP Framework Laravel, and Vue.js - see `Components` page for more details._

First off, thanks for your interest in contributing to Dopenote!

If you have any questions \(or just want to chat\), add me on discord: `xy#2222`

### Pull Requests

If you're fixing a small, obvious bug, typo or a translation, etc., just submit a pull request. Please look for existing issues or pull requests beforehand.

But if it's more complicated, you should open an issue on GitHub, before you start.

If you want to work on an existing issue, please comment before you start working on it, so others won't waste their time.

#### Commits

When you're fixing an issue created on GitHub, start your commit message with referencing the issue, followed by a short message.

Example: `#53 Added CONTRIBUTING.md file`

### Security

If you've found a vulnerability bug please email [xy2z@pm.me](mailto:xy2z@pm.me) instead of opening an issue.

### Coding Style Guide

Remember to use the `.editorconfig` file for your editor.

#### General \(php, js, html, css\)

* Encoding should always be UTF-8.
* Use 1 tab for indenting, not spaces.
* Always spaces after `if`, `while`, `for`, etc.
  * Good: `if (check) {`
  * Bad: `if( check ){`
* Function and method names are lowercase with underscore
  * ✅ Good: `function create_note() {`
  * ⛔ Bad: `function CreateNote() {`
* Classes are `CamelCase`.

#### JS specific

* Try not to use unnessecary semi colons \(read [https://flaviocopes.com/javascript-automatic-semicolon-insertion/](https://flaviocopes.com/javascript-automatic-semicolon-insertion/)\)

#### PHP specific

Use [https://www.php-fig.org/psr/psr-2/](https://www.php-fig.org/psr/psr-2/) EXCEPT for:

* Use tab instead of spaces for indenting.
* Curley braces \(`{`\) are always written on the same line as the class/method/statements.

#### 

