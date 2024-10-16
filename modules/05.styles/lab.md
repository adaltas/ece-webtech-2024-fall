---
duration: 2h
---

# Lab: getting started with TailwindCSS

Tailwind CSS is a utility-first CSS framework designed to enable users to create applications faster and easier. You can use utility classes to control the layout, color, spacing, typography, shadows, and more to create a completely custom component design — without leaving your HTML or writing a single line of custom CSS.

## Objectives

- CSS usages
- Tailwind usage and customization

## Tasks

1. Initialize Tailwind CSS inside a Next.js application (easy level)
2. Prepare your code (easy level)
3. Simple usage of Tailwind CSS (medium level)
4. Apply plugins (simple level)
5. Style the layout (hard level)
6. Custom classes with the `@apply` directive (medium level)

## Prerequisites

Tag your latest commit from the previous lab with a name like `lab4` to help navigate your project. Don't forget to push the tag.

## Part 1. Initialize Tailwind CSS inside a Next.js application (easy level)

Follow the [official installation](https://tailwindcss.com/docs/guides/nextjs) guide to install Tailwind inside Next.js. Since you already have a Next.js application, start at step 2.

## Part 2. Prepare your code (easy level)

Removing all  existing styles from your project (the imports in `/app/**` and `components/**` to `/styles/*.module.css` as well as the references to `styles`).

Make sure the `/styles/globals.css` only contains the `@tailwind` directives and nothing else.

## Part 3. Simple usage of Tailwind CSS (medium level)

Use the [Tailwind CSS documentation](https://tailwindcss.com). The `ctrl-k` shortcut popup a convenient search box.

Now, try to add some style using Tailwind to your project!

## Part 4. Apply plugins (simple level)

Install the following Tailwind CSS plugins inside the `tailwind.config.js` configuration file:

- tailwindcss-font-inter
- @tailwindcss/typography
- @tailwindcss/forms

Go back to your contact page, and the form input shall look a little better (a little better === still far from nice).

Don't forget to add the package dependencies with `npm install`.

## Part 5. Custom classes with the `@apply` directive (medium level)

To style the titles, we will create a `wt-title`. Note, "wt" stands for Web Tech.

Inside `styles/globals.css`, create the following class:

```css
.wt-title {
  @apply text-3xl font-bold underline mb-10;
}
```

In every occurence of `<h1>...</h1>` inside the `./pages` folder, add the `wt-title` class to the `className` attribute of each `h1` tag.
