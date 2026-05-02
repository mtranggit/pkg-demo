# mtd-pkg

A minimal demo package showing how to publish an NPM package using modern tooling.

## Overview

This repository contains a simple TypeScript package template with a `pnpm` workflow. It demonstrates the modern package publishing process:

- install dependencies with `pnpm`
- build the package using TypeScript
- publish to npm from a local repository

## Prerequisites

- Node.js 20+ installed
- `pnpm` installed globally
- an npm account
- `npm login` completed before publishing

## Setup

Install dependencies with pnpm:

```bash
pnpm install
```

## Build

If you want to compile the TypeScript source before publishing, run:

```bash
pnpm exec tsc
```

This project currently uses `index.ts` as its source entry point and `index.js` as the published bundle entry point.

## Publish to npm

1. Make sure the package version is correct in `package.json`.
2. Run `npm login` if you have not already authenticated.
3. Publish the package:

```bash
pnpm publish --access public
```

If you prefer npm directly, use:

```bash
npm publish --access public
```

## Notes

- The package is named `mtd-pkg` in `package.json`.
- The repository currently has no tests configured.
- Add a `description`, `repository`, and `keywords` to `package.json` to improve the package listing on npm.

## License

MIT
