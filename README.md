# npm-package-init

My personal, minimal setup for building and releasing npm packages. Please note that I'm using this on MacOS and I haven't tested it on other systems.

## Features

- Uses TypeScript by default.
- Generates both ESM and CJS modules, as well as definitions.
- Simple system for creating a demo page and releasing it to the GitHub pages.
- Minimal - only two dev dependencies: `esbuild` and `typescript`.

## Renaming the package

To rename a package you can run these two commands:

```
sed -i '' 's/npm-package-init/new-package-name/' *.json *.md src/* docs/*
```

```
sed -i '' 's/Stanko/your-github-handle/' package.json
```

## Commands

`npm start`

Runs a development server on http://localhost:8000

`npm run build`

Build the package and the demo page.
