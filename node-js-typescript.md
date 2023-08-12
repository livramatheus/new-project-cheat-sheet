# New Node.JS + TypeScript + Express project cheat sheet

This cheat sheet depicts some broad instructions on how to set up a new Node.JS + TypeScript + Express project. It's suited for those who already have some experience and just want a simple checklist for a brand new project.

This cheat sheet will guide you through:

- @todo

## Initializing Node.js Project

1. Run `npm init -y` inside the desired project folder
2. You may also fill in the project details under `package.json`

## Installing TypeScript

1. Install TypeScript as a dev dependency by running:

```bash
npm install -D typescript ts-node-dev
```

2. Now run the following to initialize TypeScript:

```bash
npx tsc --init
```

3. The previous command will generate a `tsconfig.json`, open it, and uncomment and set the `rootDir` and `outDir` as your like. `outDir` is where the converted files will sit. Example:

```json
"rootDir": "./src",
// ...
"outDir": "./dist", 
```

## Installing eslint

Source: [eslint](https://www.npmjs.com/package/eslint)

1. Run:

```bash
npm i --save-dev eslint
```

## Installing lint preset

Source: [eslint-config-rocketseat](https://github.com/Rocketseat/eslint-config-rocketseat)

1. Run:
```bash
npm i -D eslint @rocketseat/eslint-config
```
2. Create `.eslintrc.json` file in the root of the project and set it up as follows:

```json
{
  "extends": "@rocketseat/eslint-config/node"
}
```

## Installing nodemon

1. Install nodemon by running:

```bash
npm i --save-dev nodemon
```

2. Open `package.json` file and add the scripts for building, starting and debugging:

```json
"scripts": {
  "build": "npx tsc",
  "start": "node dist/index.js",
  "dev": "nodemon index.ts"
}
```

## Installing express

Source: [express](https://www.npmjs.com/package/express)

1. Install express by running:

```bash
npm i express
```

2. Install express types by running:

```bash
npm install -D @types/express
```

## Connect to a GitHub repository

1. Run `git init`
2. Create the `.gitignore` file
3. Paste into the `.gitinore` the contents of [this template](https://github.com/github/gitignore/blob/main/Node.gitignore)
4. Create the repository and add remote origin
5. Create the first commit and push files

## Testing

1. Create a file named `index.ts` under `./src` and paste the following:

```typescript
import express, { Request, Response, Application } from 'express'

const app: Application = express()
const port = process.env.PORT || 8000

app.get('/', (req: Request, res: Response) => {
  res.send('Hello world')
})

app.listen(port, () => {
  console.log(`Server is online -> http://localhost:${port}`)
})

```

2. Test `build`, `start` and `dev` scripts
