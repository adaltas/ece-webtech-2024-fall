---
duration: 2h
---

# Lab: getting started with React and Next.js

Using React together with Next.js gives you building blocks to create web applications fast. Since this lab, we start working on a skeleton of your course project, a blogging website.

## Objectives

- Next.js application initialization
- Build a website skeleton for blogging
- Build dynamic routes

## Tasks

1. Part 1. Initialize the Next.js application (easy level)
1. Part 2. Build a website skeleton for blogging (medium level)
1. Part 3. Build dynamic routes (medium level)

## Prerequisites

Tag your latest commit from the previous lab with a name like `lab3` to help navigate your project. Don't forget to push the tag.

## Part 1. Initialize the Next.js application (easy level)

Initialize a Next.js application by following [this guide](https://nextjs.org/docs/getting-started/installation) to start. Under your repository root, run the `npx create-next-app@latest` and name your application as `ui` (or `client` or `front` or other).

## Part 2. Build a website skeleton for blogging (medium level)

1. Learn [React components](https://react.dev/learn/describing-the-ui), [Next.js routing](https://nextjs.org/docs/app/building-your-application/routing/defining-routes), [Next.js pages](https://nextjs.org/docs/app/building-your-application/routing/pages) and [Next.js layouts](https://nextjs.org/docs/app/building-your-application/routing/pages-and-layouts) to continue with the next steps.
1. Create at least 3 pages for your website. One of them should contain a list of elements (that will later all have their own page). For example :

   - `/` - home page
   - `/about` - about page
   - `/contacts` - contacts page
   - `/articles` - a list of articles

   You can be inspired by any example of a blogging website, for example [Adaltas company website](https://www.adaltas.com/).
1. Create shared components like a header, a footer, and a navigation menu between pages (using [`Link` component](https://nextjs.org/docs/app/building-your-application/routing/linking-and-navigating)), and display reuse them on every page using a `layout`.

Note! Don't play a lot with CSS for this moment. We will learn a modern CSS framework ([Tailwind CSS](https://tailwindcss.com)) later.

## Part 3. Build dynamic routes (medium level)

1. Learn [dynamic routing](https://nextjs.org/docs/app/building-your-application/routing/dynamic-routes) in Next.js.
1. Build an dynamic page with a route like `/articles/:articleId`, displaying `articleId` and some dummy data.
