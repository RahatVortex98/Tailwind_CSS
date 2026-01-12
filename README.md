<h3 align='center'>Tailwind CSS</h3>


<h3 align='center'>Introduction</h3>

### ➡️ Tailwind CSS is a utility-first CSS framework. Instead of writing custom CSS rules, you compose designs directly in your HTML using predefined utility classes.

- **Traditional CSS:**

      .btn {
      padding: 12px;
      background: #2563eb;
      color: white;
      border-radius: 6px;
    }
- **Tailwind CSS:**

      <button class="px-4 py-3 bg-blue-600 text-white rounded-md"> Button</button>

<h3 align='center'>Installaion</h3>

## Option 1: Quickest way (CDN – great for prototypes)

      <!-- Tailwind CDN (v3.4+) -->
        <script src="https://cdn.tailwindcss.com"></script>
## Option 2: Local installation (recommended for serious projects)

Install dependencies

      npm install tailwindcss @tailwindcss/postcss postcss
Install Tailwind CSS v4 + CLI

      npm install -D tailwindcss @tailwindcss/cli
Create basic folder structure

      mkdir src dist
      touch src/input.css index.html
      
Add your CSS file (src/input.css)

      /* src/input.css */
      @import "tailwindcss";
      
      /* Optional: custom theme (colors, fonts, spacing, etc.) */
      @theme {
        --color-primary: #3b82f6;
        --color-primary-dark: #1d4ed8;
        --color-success: #10b981;
        
        --font-sans: "Inter var", system-ui, -apple-system, sans-serif;
      }
      
      /* Your own custom styles (optional) */


Add scripts to package.json

          {
              "name": "tailwind-css",
              "version": "1.0.0",
              "description": "Plain HTML + Tailwind CSS v4 project",
              "main": "index.js",
              "type": "commonjs",
              "license": "ISC",
              "author": "",
              "scripts": {
                "build": "npx @tailwindcss/cli -i ./src/main.css -o                                           ./dist/output.css --minify",
                "watch": "npx @tailwindcss/cli -i ./src/main.css -o                                           ./dist/output.css --watch",
                "dev": "npx @tailwindcss/cli -i ./src/main.css -o ./dist/output.css                               --watch"
              },
              "dependencies": {
                "@tailwindcss/postcss": "^4.1.18",
                "postcss": "^8.5.6",
                "tailwindcss": "^4.1.18"
              },
              "devDependencies": {
                "@tailwindcss/cli": "^4.1.18"
              }
            }
Create basic index.html

      <link href="./dist/output.css" rel="stylesheet">
Start developing

      # Development (auto rebuild on change)
      npm run dev

<h3 align='center'>Eelments</h3>

1. Spacing (padding & margin)

px-{value} → padding left & right (x-axis)

py-{value} → padding top & bottom (y-axis)

mx-{value} → margin left & right (x-axis)

my-{value} → margin top & bottom (y-axis)

p-{value} → padding on all sides

2. Colors

bg-{color}-{shade} → background color

text-{color}-{shade} → text color

Shades usually go 100 (light) → 900 (dark)

      <div class="bg-blue-500 text-white">Hello</div>
      
3. Flexbox utilities

flex → makes the element a flex container

flex-row → horizontal direction (default)

flex-col → vertical direction

space-x-{value} → horizontal space between child elements

space-y-{value} → vertical space between child elements

justify-{start|center|end|between|around|evenly} → alignment along main axis

items-{start|center|end|stretch|baseline} → alignment along cross axis

      <div class="flex justify-center items-center space-x-4">
        <div class="bg-red-500 p-2">One</div>
        <div class="bg-green-500 p-2">Two</div>
        <div class="bg-blue-500 p-2">Three</div>
      </div>
      
justify-start → align left/top

justify-center → align center

justify-end → align right/bottom

justify-between → equal space between items

justify-around → equal space around items

justify-evenly → equal space between and around items

4. Text utilities

text-{size} → font size (e.g., text-sm, text-lg, text-2xl)

font-{weight} → font weight (e.g., font-bold, font-medium)

text-{color}-{shade} → text color

5. Other useful things

rounded-{size} → border radius

border / border-{color}-{shade} → border and color

shadow / shadow-lg → box shadow

w-{value} / h-{value} → width / height


### justify-* only works on flex or grid containers.
<h3 align='center'>How Does It Work?</h3>
<h3 align='center'>Fundamental</h3>
<h3 align='center'>Just-In-Time (JIT) Compiler</h3>
<h3 align='center'>Layout & Flex-box</h3>
<h3 align='center'>Media Query & Responsive Design</h3>
<h3 align='center'>Dark Mode</h3>
<h3 align='center'>Custom Styles & Reusability</h3>
<h3 align='center'>Tips & Tricks</h3>
<h3 align='center'>Fitness Project Details</h3>
