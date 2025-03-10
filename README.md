# How to use Tailwind

Tailwind can be used in 2 main ways: using an HTML <link> tag to reference a copy on someone else's server (typically a CDN (Content Delivery Network)), or installing Tailwind in the project.

## Option A: borrow Tailwind from a public CDN

Include this in the <head> section of the HTML: `<script src="https://cdn.tailwindcss.com"></script>`. Importing from CDN is recommended for testing and drafting. Final production should use local Tailwind.

## Option B: Installing Tailwind in the project

Installing Tailwind locally is better for final production. Use these [instructions](https://tailwindcss.com/docs/installation/tailwind-cli) (reproduced below):

1. Install Node.js
2. Reboot VSCode if opened
3. Open a terminal in the root directory
4. Install via one of the methods below

### CLI (for use with raw HTML, CSS, JS)

1. Run `npm install tailwindcss @tailwindcss/cli`
2. Copy `@import "tailwindcss";` to the top of your style.css file to be able to use Tailwind directly in your CSS styles,
   then you can build your own complex classes or components using Tailwind, and mix and match with regular CSS.
3. Build the Tailwind CSS file using the CLI interface:
   `npx @tailwind/cli -i ./styles.css -o ./tailwind/styles.css`
   IMPORTANT: This file has to be rebuilt every time you change your 'styles.css'. You can use the --watch flag to make the command keep
   listening for changes. It will stay running in the terminal:
   `npx @tailwind/cli -i ./styles.css -o ./tailwind/styles.css --watch`

### Vite (for frameworks like Laravel, SvelteKit, React Router, Nuxt, SolidJS, etc)

See [instructions](https://tailwindcss.com/docs/installation/tailwind-cli).

### PostCSS (for frameworks like Next.js and Angular)

See [instructions](https://tailwindcss.com/docs/installation/tailwind-cli).


---------

Start using Tailwind! You can slap the Tailwind classes into the `classes=""` tag inside your HTML, or you can create your own classes that use Tailwind's classes.

https://tailwindcss.com/docs/styling-with-utility-classes
