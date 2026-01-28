<h2 align="center">🌬️ Tailwind CSS</h2>

---

<h3 align="center">Introduction</h3>

### ➡️ Tailwind CSS is a utility-first CSS framework. Instead of writing custom CSS rules, you compose designs directly in your HTML using predefined utility classes.

* **Traditional CSS:**

```css
.btn {
  padding: 12px;
  background: #2563eb;
  color: white;
  border-radius: 6px;
}
```

* **Tailwind CSS:**

```html
<button class="px-4 py-3 bg-blue-600 text-white rounded-md">Button</button>
```

---

<h3 align="center">Installation</h3>

## Option 1: Quickest way (CDN – great for prototypes)

```html
<!-- Tailwind CDN (v3.4+) -->
<script src="https://cdn.tailwindcss.com"></script>
```

## Option 2: Local installation (recommended for serious projects)

<h3>Simple way to start your project for V4</h3>

```bash
i) npm init -y        # initializes the directory as a Node.js project
ii) npm install -D tailwindcss postcss autoprefixer vite   # installs packages
```

### iii) Manually create Tailwind and PostCSS config files

**tailwind.config.js**

```js
/** @type {import('tailwindcss').Config} */
export default {
  content: [
    "./*.html",
    "./src/**/*.{html,js}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

**postcss.config.js**

```js
export default {
  module.exports = {
    plugins: [
      require('@tailwindcss/postcss'),
      require('autoprefixer'),
    ],
  }
}
```

### Create your CSS file (e.g., `src/input.css`) and add:

```css
/* Preflight (replaces @tailwind base) */
@import "tailwindcss/preflight";

/* Utilities (replaces @tailwind utilities) */
@tailwind utilities;
```

### iv) Add scripts in `package.json`

```json
"scripts": {
  "dev": "tailwindcss -i ./src/input.css -o ./dist/output.css --watch",
  "build": "tailwindcss -i ./src/input.css -o ./dist/output.css --minify",
  "start": "vite"
}
```

### v) Build or watch Tailwind CSS

```bash
npm run dev
```

**Build minified CSS for production:**

```bash
npm run build
```

### vii) Include generated CSS in your HTML

```html
<link href="./dist/output.css" rel="stylesheet">
<link href="./src/input.css" rel="stylesheet">
```

```txt
# for this only "npm run start" will work
```

### viii) Start Vite server (optional if using Vite for live reload)

```bash
npm run start
```

---

### Extensions
-postCss language support



<h3 align="center">Elements</h3>

## 1. Spacing (padding & margin)

* `px-{value}` → padding left & right (x-axis)
* `py-{value}` → padding top & bottom (y-axis)
* `mx-{value}` → margin left & right (x-axis)
* `my-{value}` → margin top & bottom (y-axis)
* `p-{value}` → padding on all sides

## 2. Colors

* `bg-{color}-{shade}` → background color
* `text-{color}-{shade}` → text color

Shades usually go **100 (light) → 900 (dark)**

```html
<div class="bg-blue-500 text-white">Hello</div>
```

## 3. Flexbox utilities

* `flex` → makes the element a flex container
* `flex-row` → horizontal direction (default)
* `flex-col` → vertical direction
* `space-x-{value}` → horizontal space between children
* `space-y-{value}` → vertical space between children
* `justify-{start|center|end|between|around|evenly}` → main axis alignment
* `items-{start|center|end|stretch|baseline}` → cross axis alignment

```html
<div class="flex justify-center items-center space-x-4">
  <div class="bg-red-500 p-2">One</div>
  <div class="bg-green-500 p-2">Two</div>
  <div class="bg-blue-500 p-2">Three</div>
</div>
```

**Justify options:**

* `justify-start` → align left/top
* `justify-center` → align center
* `justify-end` → align right/bottom
* `justify-between` → equal space between items
* `justify-around` → equal space around items
* `justify-evenly` → equal space between and around items

## 4. Text utilities

* `text-{size}` → font size (e.g., `text-sm`, `text-lg`, `text-2xl`)
* `font-{weight}` → font weight (e.g., `font-bold`, `font-medium`)
* `text-{color}-{shade}` → text color

## 5. Other useful things

* `rounded-{size}` → border radius
* `border` / `border-{color}-{shade}` → borders
* `shadow` / `shadow-lg` → box shadow
* `w-{value}` / `h-{value}` → width / height

> **Note:** `justify-*` only works on flex or grid containers.

> **Tip:** Use `h-screen` instead of `h-100` (Tailwind doesn’t recognize `h-100` by default).

---

<h3 align="center">Font & Sizing</h3>

* `sm` → small
* `md` → medium
* `lg` → large

### **The `font-*` Classes**

These classes change the actual identity and thickness of the letters.

* **Family:** `font-sans`, `font-serif`, `font-mono`
* **Weight:** `font-bold`, `font-light`, `font-black`
* **Style:** `italic`

### **The `text-*` Classes**

These control appearance and layout.

* **Size:** `text-sm`, `text-xl`, `text-5xl`
* **Color:** `text-blue-500`, `text-white`, `text-transparent`
* **Alignment:** `text-center`, `text-right`, `text-justify`
* **Decoration:** `underline`, `uppercase`, `lowercase`

### **Custom fonts**

**`src/input.css`**

```css
@import "tailwindcss";

@theme {
  /* This creates a new class called font-brand */
  --font-brand: "Poppins", sans-serif;

  /* This overwrites the default font-sans with Inter */
  --font-sans: "Inter", ui-sans-serif, system-ui;
}
```

---

<h3 align="center">Margin, Borders & Padding</h3>

<h3 align="center">Fundamental</h3>
<h3 align="center">Just-In-Time (JIT) Compiler</h3>
<h3 align="center">Layout & Flex-box</h3>
<h3 align="center">Media Query & Responsive Design</h3>
<h3 align="center">Dark Mode</h3>
<h3 align="center">Custom Styles & Reusability</h3>
<h3 align="center">Tips & Tricks</h3>
<h3 align="center">Fitness Project Details</h3>
