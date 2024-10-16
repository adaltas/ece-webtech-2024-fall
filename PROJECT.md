
# Project instructions

You are tasked with creating a digital publishing application to showcase the knowledge acquired during the semester.

Your application can be anything that meets the requirements below (blog, cooking recipes, travel journal, ...). Its key features include:

* **User Authentication**: Implement a robust OAuth2 authentication system for user login, utilizing an external provider.
* **Content Management**: Empower users to create, publish, and store posts within a structured database.
* **Community Interaction**: Develop a feature for users to comment on posts, enabling lively discussions and interactions.
* **Navigation and Accessibility** : Design an intuitive interface for users to easily navigate through posts and comments.
* **User Profile Customization**: Provide users with the functionality to manage and personalize their profiles and settings.

Consider drawing inspiration from platforms like [Medium](https://medium.com/creators) or [Hacker News](https://news.ycombinator.com/).

## Deadline

Coming soon...

## Delivery Requirements

* **GitHub Repository**: Submit your project on GitHub (keep the repository from labs). Keep it private and grant access to your instructor.
* **Deployment**: Deploy your application on [Vercel.com](https://vercel.com) and [Supabase.com](https://supabase.com/) with a publicly accessible URL.
* **Repository Structure**: Organize your repository as follows:
  
  ```txt
  /
  ├── client/       # or front/, etc. - Frontend made using Next.js
  ├── api/          # or back/, api/, etc. - Backend made using Node.js/Express
  ├── supabase/     # Supabase Docker Compose configuration
  ├── README.md
  ├── .gitignore    # (optional) Global .gitignore for DS_Store, etc.
  └── ...           # (optional) Other files and directories like labs notes, LICENSE, etc.
  ```

* **Documentation**: Your `README.md` must follow the provided [template](./project-template/README.md). In particular, it must include a self-evaluation and **concise** comments on your implementation.

## Technological Restrictions

Following the course's philosophy:

* Do not use frameworks other than Next.js.
* Supabase must be the only storage solution.
* Tailwind CSS is the exclusive CSS framework.

Bonus tasks are exempt from these restrictions.

## Evaluation

* Each task is graded based on difficulty (easy = 2, medium = 4, hard = 6).
* Tasks must be functional (at least partially) and documented in `README.md` to be evaluated.
* Maximum score: 60 points (equivalent to grade 20).
* Bonus points can be awarded for going beyond the core requirements, capped at 10% of the maximum score.
* **Will be penalized with a 0:**
  * Plagiarism.
  * Missing delivery requirements.
  * Not respecting the technological restrictions.
  * Insuficient participation in the group.
* Improper use of AI tools will lead to more stringent evaluation.

A [project template](./project-template) is provided to help you get started. However, we recommend continuing on the project used for the labs.

If any doubts, post an issue on the course GitHub repository.

## Tasks

### Project management

* **Naming convention**
  * 2 points (easy)
  * Follow the community conventions and best practices, consistency.
* **Project structure**
  * 2 points (easy)
  * Simplicity and comprehensiveness, files/components/layout organization.
* **Git usage**
  * 2 points (easy)
  * Proper commit history respecting [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/), squashing bad commits, meaningful commit messages...
* **Code quality**
  * 4 points (medium)
  * Indentation, understandability, line spacing, comments... Use of a formatter or linter is a plus.
* **Design, UX, and content**
  * 4 points (medium)
  * Overall look and feel, user experience (UX), the responsiveness on all screens, meaningful content. Good usage of Tailwind CSS. You are allowed to use Tailwind-based component libraries like [Tailwind UI](https://tailwindui.com), [Flowbite](https://flowbite.com/), [Headless UI](https://headlessui.com/)...

### Application development

* **Home page**
  * 2 points (easy)
  * Make the home page friendly, good-looking, informative, and with a call to action (CTA). Refer to other websites on the web to take inspiration and provide relevant information about your project. This task is mostly about content editing and design. The [Medium](https://medium.com/) or [Adaltas](https://www.adaltas.com/) homepages are good examples.  
  It is recommended to prototype your design first in a graphical editor like [Figma](https://www.figma.com/) or [Gravit Designer](https://www.designer.io/en/), then code it.
* **Navigation**
  * 2 points (easy)
  * The application must contain a navigation bar with links to several pages (home, about, contact, ...). A common layout must be shared between all pages.
* **Login and profile page**
  * 4 points (medium)
  * Provide a login/logout button in the header. On login, open the login page with a signin/signup form with GitHub provider using Auth component of Supabase. Persist authenticated user information in React context and display it on the profile page and the header.
* **Post creation and display**
  * 6 points (hard)
  * Allow the creation of post for authenticated user on your app. Open a page with a form with the post properties (`title`, `content`, `categories`, `tags`, ...). Propose to cancel or save the form, and persist the article in the database. Display the list of posts on a dedicated page. The list must be paginated and sorted by creation date. Each post must be displayed on its own page with its content and comments. Posts are public and can be accessed by anyone. Only authenticated users can create posts.
* **Comment creation and display**
  * 4 points (medium)
  * Display a form at the bottom of post pages allowing users to leave a comment. You can be inspired by commenting on GitHub issues. Users must at least provide a `content` and `email` properties. You can be inspired by commenting on GitHub issues.
* **Post modification and removal**
  * 4 points (medium)
  * Once a post is created, only the author can see the "edit" button, redirecting to the editing page to modify the post. The author can also remove the post.
* **Search**
  * 6 points (hard)
  * Create a search bar allowing the user to search for posts. The search must be performed on the server-side (use the Full Text Search capabilities of Supabase).
* **Use an external API**
  * 2 points (easy)
  * Use an external API to enrich the content of your application. For example, you can use the [Unsplash API](https://unsplash.com/developers) to display a random image to illustrate your posts, fetch pokemon data from the [PokeAPI](https://pokeapi.co/), display a random quote from the [Quote Garden API](https://pprathameshmore.github.io/QuoteGarden/)...
* **Resource access control**
  * 6 points (hard)
  * Make your application datas secure by default. It must use the RLS of Supabase to prevent unexpected access and intrusion attempts. Only authenticated users can create posts. A user must only gain access to its own content. The API must return the appropriate lists for the authenticated user. The HTTP response must return an appropriate HTTP response code and message.
* **Account settings**
  * 4 points (medium)
  * Create a dashboard for the user to modify his/her personal settings (email, name, language, profile picture...). You don't have to make these settings active, the goal is to display and load form various components type. If you do, it is part of the bonus and you must mention it in the README, you can refer to [this guide of managing user data in Supabase](https://supabase.com/docs/guides/auth/managing-user-data).
* **WYSIWYG integration**
  * 2 points (easy)
  * The `content` input fields for posts are featured with any [WYSIWYG](https://en.wikipedia.org/wiki/WYSIWYG) library to edit its content.
* **Gravatar integration**
  * 2 points (easy)
  * Display a Gravatar user icon right next to his comments, in the header, and on the profile page. [Gravatar](https://en.gravatar.com/) is a service that associates your email with an image you upload. Other services may then refer to it. Some people choose a photo of themself, while others use an abstract image. It is part of the tech culture and services such as GitHub and NPM.js use it. It is very easy to integrate and it will provide a default random image if the user email is not registered.
* **Light/dark mode**
  * 2 points (easy)
  * Implement switching between light and dark themes using Tailwind CSS and persist the setting for the user session.

## Bonus

Document any bonus features in your README.md. Here are some ideas:

* Admin dashboard to manage users and posts.
* Add likes and/or reactions on posts.
* Add nested comments.
* Implement a digital version of your resume.
* DevOps: Implementing Docker and Docker Compose to start the application and the storage.
* Any feature of your liking...

> [!TIP]  
> +1 bonus point will be awarded if you provide **meaningful** feedback about the course (content, structure, labs, subjects you enjoyed/disliked/missed...).
