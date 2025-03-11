# How to use Tailwind

Tailwind can be used in 2 main ways: using a public CDN (content delivery network) available online, or installing Tailwind in the project.

## Option A: Use a public CDN

Include this in the <head> section of the HTML: `<script src="https://cdn.tailwindcss.com"></script>`. Importing from CDN is recommended for testing and drafting. Final production should use local Tailwind.

```html
<html>
   <head>
      <script src="https://cdn.tailwindcss.com"></script>
   </head>
   <body>
      <div class="insert tailwind classes here separated by spaces">
         <div> Stuff </div>
         <div> Stuff </div>
      </div>
   </body
</html>
```

## Option B: Install Tailwind in the project

Installing Tailwind locally provides faster loading and guarantees your website looks the same, even if Tailwind releases an update that changes their classes. Tailwind scans your HTML and CSS files and generates a new Tailwind CSS file that contains only the subset of features you use from Tailwind, ensuring that your website loads only what you need.

1. Install Node.js
2. Reboot VSCode if open, to reload PATH variables that Node installer modified.
3. Open a terminal and navigate to the project main directory
4. Install using the instructions below (tailored for our project).

CLI (for use with raw HTML, CSS, JS):

[source](https://tailwindcss.com/docs/installation/tailwind-cli)

1. Run `npm install tailwindcss @tailwindcss/cli`
2. Copy `@import "tailwindcss";` into the top of your style.css file to be able to use Tailwind directly in your CSS styles,
   then you can build your own complex classes or components using Tailwind, and mix and match with regular CSS.
3. Build the Tailwind CSS file using the CLI interface:
   `npx @tailwind/cli -i ./styles.css -o ./tailwind/styles.css`
   IMPORTANT: This file has to be rebuilt every time you change your 'styles.css'. You can use the --watch flag to make the command keep
   listening for changes. It will stay running in the terminal:
   `npx @tailwind/cli -i ./styles.css -o ./tailwind/styles.css --watch`

Vite (for frameworks like Laravel, SvelteKit, React Router, Nuxt, SolidJS, etc):

[source](https://tailwindcss.com/docs/installation/using-vite).

PostCSS (for frameworks like Next.js and Angular):

[source](https://tailwindcss.com/docs/installation/using-postcss).


---------

Start using Tailwind! You can slap the Tailwind classes into the `classes=""` tag inside your HTML, or you can create your own classes that use Tailwind's classes.

https://tailwindcss.com/docs/styling-with-utility-classes
