<h1 align="center">dotfile_bolilerplate</h1>

<p align="center">
  <strong>A curated collection of configuration boilerplates</strong><br>
  Every option is commented for clarity — copy, adapt, ship.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License: MIT" />
  <img src="https://img.shields.io/badge/editor-VSCode-007ACC.svg" alt="Editor: VSCode" />
  <img src="https://img.shields.io/badge/formatter-Biome-60A5FA.svg" alt="Formatter: Biome" />
  <img src="https://img.shields.io/badge/formatter-Prettier-F7B93E.svg" alt="Formatter: Prettier" />
</p>

---

## Philosophy

This repo is a **living reference** of tool configurations I use across projects. Rather than starting from scratch every time, I keep well-documented boilerplates here so I can grab what I need.

> [!NOTE]
> This is **not** a buildable or runnable project. Files here are meant to be copied into other projects and adapted.

## What's Inside

### Formatter & Linter

| File | Description |
|------|-------------|
| [`.prettierrc`](.prettierrc) | Prettier config — single quotes, 2-space indent, 100 char width. Includes `prettier-plugin-tailwindcss`. |
| [`biome.json`](biome.json) | Biome config — formatting, linting, and import organizing. Single quotes, semicolons, 2-space indent, 100 char width. |

### Editor

| File | Description |
|------|-------------|
| [`.vscode/settings.json`](.vscode/settings.json) | VSCode workspace settings — Biome as default formatter, format on save, 100-char ruler, TailwindCSS quick suggestions, Rust & Python overrides. |

### Reference

| File | Description |
|------|-------------|
| [`agent_requirements.md`](agent_requirements.md) | Coding conventions and project structure guidelines for Rust projects. |

## Quick Start

Pick the configs you need and drop them into your project:

```bash
# Clone the repo
git clone https://github.com/chho/dotfile_bolilerplate.git

# Copy what you need
cp dotfile_bolilerplate/biome.json ./your-project/
cp dotfile_bolilerplate/.prettierrc ./your-project/
cp -r dotfile_bolilerplate/.vscode ./your-project/
```

## Formatting

Run Prettier across the repo:

```bash
npx prettier --write .
```

Or let Biome handle it:

```bash
npx @biomejs/biome format --write .
npx @biomejs/biome check --write .
```

## License

[MIT](LICENSE) &copy; Hao
