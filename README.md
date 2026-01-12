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

<h3>simple way to start your project for V4</h3>

      i) npm init -y // this initialized the directory as a Node.js project
      
      ii) npm install -D tailwindcss postcss autoprefixer vite //installs packages
      
      iii) Manually create Tailwind and PostCSS config files
      
            -tailwind.config.js:
            
            /** @type {import('tailwindcss').Config} */
                  export default {
                    content: [
                      "./*.html",
                      "./src/**/*.{html,js}"
                    ],
                    theme: {
                      extend: {},
                    },
                    plugins: [],
                  }
                  
            -postcss.config.js:
            
            export default {
                    module.exports = {
                    plugins: [
                      require('@tailwindcss/postcss'),
                      require('autoprefixer'),
                    ],
                  }

           -Create your CSS file (e.g., src/input.css) and add:
           
                 /* Preflight (replaces @tailwind base) */
                  @import "tailwindcss/preflight";
                  
                  /* Utilities (replaces @tailwind utilities) */
                  @tailwind utilities;


      iv)Add scripts in package.json:

            "scripts": {
              "dev": "tailwindcss -i ./src/input.css -o ./dist/output.css --watch",
              "build": "tailwindcss -i ./src/input.css -o ./dist/output.css --minify",
              "start": "vite"
            }

             
      
      v)Build or watch Tailwind CSS
      
            npm run dev
            
       Build minified CSS for production:

             npm run build
             
      vii)Include generated CSS in your HTML:

            <link href="./dist/output.css" rel="stylesheet">

     viii)Start Vite server (optional if using Vite for live reload):

           npm run start

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


- ** justify-* only works on flex or grid containers. **
- **Use h-screen instead of h-100 (Tailwind doesn’t recognize h-100 by default) to make the section full viewport height. **




<h3 align='center'>How Does It Work?</h3>
<h3 align='center'>Fundamental</h3>
<h3 align='center'>Just-In-Time (JIT) Compiler</h3>
<h3 align='center'>Layout & Flex-box</h3>
<h3 align='center'>Media Query & Responsive Design</h3>
<h3 align='center'>Dark Mode</h3>
<h3 align='center'>Custom Styles & Reusability</h3>
<h3 align='center'>Tips & Tricks</h3>
<h3 align='center'>Fitness Project Details</h3>
