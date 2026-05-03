# AGENTS.md

## What this repo is

A collection of configuration boilerplate files (editorconfig, prettier, tailwind, Cargo.toml, etc.). It is **not** a buildable or runnable project.

- `package.json`, `Cargo.toml`, `index.html` are template files to be copied/adapted, not active code.
- No build, test, lint, or typecheck commands exist. `npm test` exits with an error by design.

## Commit conventions

- Commit messages must follow [Conventional Commits](https://www.conventionalcommits.org/) — enforced by Husky + commitlint (`@commitlint/config-conventional`).

## Formatting

- Prettier is configured in `.prettierrc`. Run `npx prettier --write .` to format.
- Key settings: tabWidth 4, single quotes, trailing commas (`all`), printWidth 100. Markdown files use tabWidth 2.

## Notes

- The repo name contains a typo (`bolilerplate` instead of `boilerplate`). Do not rename it.
