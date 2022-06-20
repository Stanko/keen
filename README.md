# keen

My personal, minimal setup for building and releasing npm packages. Please note that I'm using this on MacOS and I haven't tested it on other systems.

![Commander Keen](./keen.png)

## Features

- Uses TypeScript by default.
- Generates both ESM and CJS modules, as well as type definitions.
- Simple system for creating a demo/docs page and deploying it to the GitHub pages.
- Minimal - only two dev dependencies: `esbuild` and `typescript`.
- Builds everything automatically before `npm publish`.

## Renaming the package

To rename a package you can run this command:

```
sed -i '' 's/keen/new-package-name/' *.json *.md src/* docs/*
```

You probably want to replace my GitHub handle as well:

```
sed -i '' 's/Stanko/your-github-handle/' package.json
```

And the last thing, open [docs/index.html](./docs/index.html) and swap my domain `muffinman.io` for yours.

## Commands

`npm start`

Runs a development server on http://localhost:8000

`npm run build`

Builds the package and the demo/docs page.

## Deploying to GitHub pages

Fist build and commit `docs/build` folder. Then in GitHub Pages settings select your branch and `/docs` folder.
