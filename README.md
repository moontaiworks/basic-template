# @moontaiworks/basic-template

[![NPM Version](https://img.shields.io/npm/v/@moontaiworks/basic-template)](https://www.npmjs.com/package/@moontaiworks/basic-template)
[![NPM Downloads](https://img.shields.io/npm/d18m/@moontaiworks/basic-template)](https://www.npmjs.com/package/@moontaiworks/basic-template)
[![Codecov](https://codecov.io/gh/moontaiworks/basic-template/graph/badge.svg)](https://codecov.io/gh/moontaiworks/basic-template)

## Features

- [x] TypeScript
- [x] [Vitest](https://github.com/vitest-dev/vitest): Tests and [Coverage](https://github.com/vitest-dev/vitest/tree/main/packages/coverage-v8)
- [x] [ESLint](https://eslint.org) + [Prettier](https://prettier.io): Coding Style & Formatter
  - [Husky](https://github.com/typicode/husky) + [Lint-staged](https://github.com/okonet/lint-staged): Pre-commit hooks
  - Auto sort and organize imports and objects by [Perfectionist](https://github.com/azat-io/eslint-plugin-perfectionist).
- [x] [Commitlint](https://github.com/conventional-changelog/commitlint): Commit message linting to follow [Conventional Commits](https://www.conventionalcommits.org)
- [x] Auto versioning, Changelog and Release to GitHub release and NPM by using [commit-and-tag-version](https://github.com/absolute-version/commit-and-tag-version)
  - Version is bumped by parsing conventional commit messages
  - Changelog is generated based on the commit messages
- [x] Show code coverage by uploading to [CodeCov](https://codecov.io) when running deployment workflow
- [x] [Typedoc](https://github.com/TypeStrong/typedoc): API documentation

## Getting Started

### 1. Use this template to create a new repository.

Click the [`Use this template`](https://github.com/new?template_name=basic-template&template_owner=moontaiworks) button on the top right corner of the repository page.

### 2. Clone the repository, and install the dependencies.

Just clone your repo and install the dependencies with any package manager you like. This template does not strong bind to any package manager, but the used package manager in GitHub Actions workflow is `pnpm`. You may need to modify the workflow file if you use other package managers.

### 3. Modify the package content to fit your project.

There are few places you need to modify to fit your project, like `package.json`, `README.md`. You can use the following command to replace most of the content:

```bash
YOUR_GITHUB_USER="your-user-name"
YOUR_REPO_NAME="your-awesome-package-name"
sed -i "s/moontaiworks/${YOUR_GITHUB_USER}/g" package.json README.md .github/workflows/*
sed -i "s/basic-template/${YOUR_REPO_NAME}/g" package.json README.md .github/workflows/*
rm -rf src/calculator tests/calculator tests/shared
echo "" > src/index.ts
```

### 4. Start coding!

## Publish

This template uses [CodeCov](https://docs.codecov.com/docs/quick-start) to check the code coverage. You can remove the CodeCov badge and the related scripts in `package.json` if you don't need it.
If you want to use CodeCov, you need to set the `CODECOV_TOKEN` in the [repository secrets](https://github.com/moontaiworks/basic-template/settings/secrets/actions).

Once you done, you can push your codes to the `main` branch.

The actions in this template will auto perform following steps when you push the code to the `main` branch:

- Test: Run tests and generate coverage report
- Build: Generate bundled and minified esm, cjs version (for browser), and unminified esm version (for node).
- Release: Bump Version & Generate Changelog
- [Publish the package to npm](https://www.npmjs.com/package/@moontaiworks/basic-template/)
- [Publish docs to GitHub Pages](https://moontaiworks.github.io/basic-template/): You may need to setup the GitHub Pages in the repository settings.

You can modify the workflow file to fit your needs.

## Install

### NPM

```bash
npm install @moontaiworks/basic-template
```

### Yarn

```bash
yarn add @moontaiworks/basic-template
```

### PNPM

```bash
pnpm add @moontaiworks/basic-template
```

## Usage

```typescript
import { ... } from "@moontaiworks/basic-template";

// ...
```

## API Document

See the [API documentation](https://moontaiworks.github.io/basic-template/).
