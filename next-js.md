# New Next.JS + TailwindCSS project cheat sheet

This cheat sheet depicts some broad instructions on how to set up a new Next.JS + TailwindCSS. It's suited for those who already have some experience and just want a simple checklist for a brand new project.

This cheat sheet will guide you through:

- Initializing a Next.js project
- Installing a lint preset
- Installing prettier plugin for Tailwind
- Cleaning default files and folders from Next.js
- Connecting the project to GitHub
- Creating Production and Test environments on Vercel

## Initializing Next.js Project
1. Run the following command inside the desired project folder

```bash
npx create-next-app@latest .
``` 

## Installing lint preset

There is no need to install eslint, it comes packaged with Next.js installation.

Source: [eslint-config-rocketseat](https://github.com/Rocketseat/eslint-config-rocketseat)

1. Run

```bash
npm i -D eslint @rocketseat/eslint-config
```

2. Set up the preset inside `.eslintrc.json`:

```json
{
  "extends": [
    "@rocketseat/eslint-config/next", 
    "next/core-web-vitals"
  ]
}
```

## Installing prettier plugin for Tailwind

Source: [prettier-plugin-tailwindcss](https://github.com/tailwindlabs/prettier-plugin-tailwindcss)

1. Run 

```bash
npm install -D prettier-plugin-tailwindcss
```

2. Create `prettier.config.js` file on project root
3. Paste the following inside this file:

```js
module.exports = {
  plugins: ['prettier-plugin-tailwindcss'],
}
``` 

## Clean default files/folders

1. Clean `/public` folder and add a `.gitkeep` file
2. Keep only tailwind declarataions on `/app/globals.css`
3. Clean up `/app/page.tsx` file

## Connect to a GitHub repository

1. Create the repository and add remote origin
2. Create the first commit and push files

## Creating Production and Test environments on Vercel

1. Create a `test` branch out of `main` branch on GitHub
2. On Vercel, create a new project and link it to the GitHub repository
3. Run the first build on Vercel
4. Under the projects settings on Vercel, click on "Settings" and then click on "Domains"
5. Fill the domain, such as "test-my-app-123.vercel.app" and click on "Add"
6. Set the "Git Branch" field to the previously created `test` branch
