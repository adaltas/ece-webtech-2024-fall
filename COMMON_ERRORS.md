# Common errors

Here is a list of common errors:

1. Poorly organized README.md   

  - Use markdown syntax (inline code, code blocks, headers etc.) - https://guides.github.com/features/mastering-markdown/
  - Write a good README with - https://dev.to/scottydocs/how-to-write-a-kickass-readme-5af9

2. Bad naming (files, functions, variables)
  - never use spaces nor accents
  - Use camelCase, kebab-case, snake_case, ... consistently
  - Choose short and meaningful names
  - Read naming convention - https://en.wikipedia.org/wiki/Naming_convention_(programming)
  
3. Dirty package.json

  - Fill the package.json with the required info
  - Use `scripts` object to define scripts which run your app.
  - Clean unnecessary dependencies
  - Start with `npm init` or `yarn init`
  - Read package.json documentation - https://docs.npmjs.com/files/package.json

4. Clean up your GitHub repository

  - Use .gitignore (exclude node_modules, .DS_Store, etc.)
  - Remove all unused and generated files (bootstrap-reboot.css, …)

5. Split your code (public, test, lib folders at root)

# Administrative issues

1. Put all the projects into one GitHub repository

The structure could be like:

```markdown
- lab-1-hello
  - src
  - README.md
  - package.json
  - ...
- lab-2-express
  - src
  - README.md
  - package.json
  - ...
- lab-2-typescript
  - src
  - README.md
  - package.json
  - ...
- ...
README.md
.gitignore
```
