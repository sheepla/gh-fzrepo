# 🚀 gh-fzrepo

<div align="right">
    <img src="https://img.shields.io/static/v1?label=Language&message=Shell&color=blue&style=flat-square"/>
    <img src="https://img.shields.io/static/v1?label=License&message=MIT&color=blue&style=flat-square"/>
</div>

An extension for [GitHub CLI](https://github.com/cli/cli) to browse repositories with fzf

## Features

- [x] Quickly browse the README of each repository
- [x] Open URL of the repository in your default browser immediately

## Usage

```
gh fzrepo -- An extension for GitHub CLI to browse repositories with fzf

USAGE
    gh-fzrepo KEYWORDS...
    gh-fzrepo -h|--help
    gh-fzrepo -V|--version
```

### Keybindings

| key | function |
|-----|----------|
| `Ctrl+J`, `Ctrl+N` | move focus down |
| `Ctrl+K`, `Ctrl+P` | move focus up |
| `Enter` | view README with `gh repo view` |
| `Ctrl+O` | open URL of the repository in your default browser | 
| `Esc`, `q` | quit fzf | 

## Installation

Dependences:

- [GitHub CLI](https://github.com/cli/cli) v2.0.0+
- [junegunn/fzf](https://github.com/junegunn/fzf)

```bash
gh extension install sheepla/gh-fzopen
```

## Contribution

Welcome!

