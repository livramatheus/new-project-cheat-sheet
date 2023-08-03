# New Next.JS + TailwindCSS project cheat sheet

### Initializing Next.js Project
1. Run `npx create-next-app@latest .` inside the desired project folder

### Installing lint preset
*`https://github.com/Rocketseat/eslint-config-rocketseat`*

1. Run `npm i -D eslint @rocketseat/eslint-config`
2. Inside .eslintrc.json:

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
