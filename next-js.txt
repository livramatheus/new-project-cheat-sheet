# New Next.JS + TailwindCSS project cheat sheet

### Initializing Next.js Project
1. Run `npx create-next-app@latest .` inside the desired project folder

### Installing lint preset
*`https://github.com/Rocketseat/eslint-config-rocketseat`*

1. Run `npm i -D eslint @rocketseat/eslint-config`
2. Inside `.eslintrc.json`:

```json
{
  "extends": [
    "@rocketseat/eslint-config/next", 
    "next/core-web-vitals"
  ]
}
```

### Installing prettier plugin for Tailwind
*`https://github.com/tailwindlabs/prettier-plugin-tailwindcss`*

1. Run `npm install -D prettier-plugin-tailwindcss`
2. Create `prettier.config.js` file on project root
3. Paste the following inside this file:

```js
module.exports = {
  plugins: ['prettier-plugin-tailwindcss'],
}
``` 

### Clean default files/folders

- Clean `/public` folder and add a `.gitkeep` file
- Keep only tailwind declarataions on `/app/globals.css`
- Clean up `/app/page.tsx` file

### Connect to a GitHub repository

- Create the repository and add remote origin
- Create the first commit and push files

### Creating Production and Test environments on Vercel

- Create a `test` branch out of `main` branch on GitHub
- On Vercel, create a new project and link it to the GitHub repository
- Run the first build on Vercel
- Under the projects settings on Vercel, click on "Settings" and then click on "Domains"
- Fill the domain, such as "test-my-app-123.vercel.app" and click on "Add"
- Set the "Git Branch" field to the previously created `test` branch
