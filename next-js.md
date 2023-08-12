# New Next.JS + TailwindCSS project cheat sheet

## Initializing Next.js Project
1. Run `npx create-next-app@latest .` inside the desired project folder

## Installing lint preset

There is no need to install eslint, it comes packaged with Next.js installation.

Source: [eslint-config-rocketseat](https://github.com/Rocketseat/eslint-config-rocketseat)

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

## Installing prettier plugin for Tailwind

Source: [prettier-plugin-tailwindcss](https://github.com/tailwindlabs/prettier-plugin-tailwindcss)

1. Run `npm install -D prettier-plugin-tailwindcss`
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
