---
duration: 2h
---

# Lab: data fetching and rendering with Next.js

In Next.js, using the appropriate data fetching strategy is key. Its impacts include:

- The performances of your page generation
- The deployment method
- The geographical distribution of your data with a CDN
- Page security, expositing publicly or not some particular URLs
- User experience
- Search Engine Optimisation (SEO)

## Objectives

- Understanding the various fetching strategies
- Practicing React and Next.js

## Tasks

1. Use SSG (medium level)
2. Build application (easy level)
3. Create profile API and use it (hard level)

## Prerequisites

Implementation of fetching strategies varies between App and Pages routers. Instructions below are given for the [Pages router](https://nextjs.org/docs/pages/building-your-application/data-fetching). If you use App router, follow [this documentation](https://nextjs.org/docs/app/building-your-application/data-fetching).

## Part 1. Use SSG (medium level)

Revit the `/pages/articles.js` page. It is currently implemented with CSR. At the moment, the generated page doesn't contain the articles at build time, including the link to individual article pages. The search engine will not be able to index the article pages.

Re-implement the page to use SSG by removing the `useEffect` function and exporting an implementation of the [`getStaticProps` function](https://nextjs.org/docs/basic-features/data-fetching/get-static-props).

## Part 2. Build application (easy level)

[Build your application](https://nextjs.org/docs/deployment) and start it. Find a method to validate that the articles are generated at build time.

You might have errors on `npm run build` related to hardcoded URL `http://localhost:3000/` for fetching data. If so, skip building application, we will do it again at the end of the course.

## Part 3. Create profile API and use it (hard level)

Create a new API endpoint available at `http://localhost:3000/api/profile`. It assumes the user is logged in and it always returns his profile information.

In the `Header` component, implement inside a `useEffect` React hook a call to fetch the profile. If the user is logged in, the API returns an object with the user's `username` and `email`. In real life, if the user is not logged in, an HTTP error 401 is returned. On success, display an account icon associated with the user's `username`.
