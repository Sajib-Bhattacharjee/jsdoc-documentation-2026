# 📘 JSDoc Documentation

<p align="center">
  <img src="images/jsdoc_logo.png" alt="JSDoc" title="JSDoc" width="100%" height="100%" />
</p>

<div align="center">

## 🚀 `JSDoc Documentation Guide`

</div>

---

## 📑 Table of Contents

1. [👋 Welcome](#-welcome)
2. [📌 Introduction](#-introduction)
3. [📦 Installing JSDoc](#-installing-jsdoc)
4. [⚙️ Configuring JSDoc](#-configuring-jsdoc)
5. [📂 Running JSDoc](#-running-jsdoc)
6. [📈 Output](#-output)
7. [🧪 Examples](#-examples)
8. [📚 Resources](#-resources)
9. [🖋️ Credits](#-credits)

---

## 👋 Welcome

Hello Everyone! I'm **`Sajib Bhattacharjee`**, a passionate **Full-Stack Web Developer** 👨‍💻.

Welcome to **`JSDoc Documentation`**, a simple yet powerful guideline for documenting your JavaScript code 🧾.

---

## 📌 Introduction

```js
// 📖 Why documentation?
// Documentation makes code easier to understand, debug, maintain, and share.
// It benefits new and senior developers alike by explaining what each piece of code does.
```

> **JSDoc** is an API documentation generator for JavaScript — like JavaDoc for Java or docstrings in Python.

Just write special comments in your code, and JSDoc will turn them into a beautiful HTML documentation site 🌐.

---

## 📦 Installing JSDoc

🔧 **Globally Install JSDoc**

```bash
npm install -g jsdoc
```

🔧 **Or as Dev Dependency**

```bash
npm install -D jsdoc
```

---

## ⚙️ Configuring JSDoc

Update your `package.json` under scripts:

```json
"scripts": {
  "jsdoc": "jsdoc -c jsdoc.json"
}
```

Create a configuration file `jsdoc.json` in your root directory:

```json
{
  "plugins": ["plugins/markdown"],
  "recurseDepth": 10,
  "source": {
    "include": ["src"],
    "includePattern": ".js$",
    "excludePattern": "(node_modules/|docs)"
  },
  "templates": {
    "cleverLinks": true,
    "monospaceLinks": true
  },
  "opts": {
    "destination": "./jsdoc",
    "recurse": true,
    "readme": "./readme.md"
  }
}
```

✅ **Explanation:**

- 📝 Enables Markdown
- 🔍 Searches up to 10 levels deep
- 📁 Includes files in the `src` directory
- 📃 Targets `.js`, `.jsx`, and `.jsdoc` files
- 🚫 Excludes `node_modules` and `docs`
- 🎨 Custom template styles
- 📤 Output goes to `./jsdoc` folder

---

## 📂 Running JSDoc

Create a file `index.js` in `src/` and add:

```js
/**
 * Site Name
 * @type {string}
 */
const siteName = "GeeksForGeeks";
```

💡 VSCode IntelliSense will help you auto-generate the JSDoc comment block!

🎯 Run JSDoc with:

```bash
npm run jsdoc
```

📁 A `jsdoc/` folder with `index.html` will be generated. Open it in your browser to view the docs.

![Generated Output](https://media.geeksforgeeks.org/wp-content/uploads/20211018023859/GeneratedDocumentationjsodc.png)

---

## 🧪 Examples

### 📦 Variables

```js
/**
 * user's fullName
 * @type {string}
 */
const fullName = "Sajib Bhattacharjee";

/**
 * Array of users
 * @type {Array}
 */
const users1 = ["Sajib Bhattacharjee", "Zahan", "Nayela"];

/**
 * Array of users age
 * @type {Array<number>}
 */
const users2 = [24, 32, 18];

/**
 * user details
 * @type {{name: string|number, age: number}}
 */
const user = {
  name: "Zahan",
  age: 32,
};

/**
 * user details
 * @type {Array<{name: string, age: number}>}
 */
const users = [
  { name: "Zahan", age: 32 },
  { name: "Nayela", age: 31 }
];
```

### 🧠 Functions

```js
/**
 * calculates the area of nothing
 * @returns {string} a simple text
 */
function areaOfNothing() {
  return "area of nothing";
}

/**
 * calculates the area of triangle
 * @param {*} dim1 - base of triangle
 * @param {*} dim2 - height of triangle
 * @returns {number} area of triangle
 */
function areaOfTriangle(dim1, dim2) {
  return 0.5 * dim1 * dim2;
}

/**
 * calculates the area of rectangle
 * @param {*} dim1 - length
 * @param {*} dim2 - width
 * @returns {number} area of rectangle
 */
function areaOfRectangle(dim1, dim2) {
  return dim1 * dim2;
}

/**
 * calculates the area of circle
 * @param {*} dim1 - radius
 * @returns {number} area of circle
 */
function areaOfcirCle(dim1) {
  return Math.PI * dim1 * dim1;
}
```

### 📤 Module Export

```js
/**
 * description
 * @module fileName
 */

/**
 * find sum of 2 numbers
 * @param {number} num1 - first number
 * @param {number} num2 - second number
 * @returns {number} sum of 2 numbers
 */
export.sum = (num1, num2) => {
  return num1 + num2;
};

// Import in another file
const { sum } = require('./fileName');
```

---

## 📚 Resources

- 🌐 [JSDoc Official Website](https://jsdoc.app/index.html)
- 📖 [GeeksForGeeks JSDoc Tutorial](https://www.geeksforgeeks.org/introduction-to-jsdoc/)

---

## 🖋️ Credits

**👨‍💻 Created & Maintained By:**  
**`Sajib Bhattacharjee`**

💖 _Dedicated to_ **"Sir! Anisul Islam"** 💖

> **All rights reserved** © Sajib Bhattacharjee, 2025

---

<div align="center">
  🎉✨ _Thanks A Lot For Visiting! Happy Coding!_ ✨🎉
</div>

