# 🚀 gh-fzrepo

<div align="right">
    <img src="https://img.shields.io/static/v1?label=Language&message=Shell&color=blue&style=flat-square"/>
    <img src="https://img.shields.io/static/v1?label=License&message=MIT&color=blue&style=flat-square"/>
</div>

An extension for [GitHub CLI](https://github.com/cli/cli) to browse and clone repositories with fzf

## Demo on asciinema.org

> [https://asciinema.org/a/435075](https://asciinema.org/a/435075)

[![asciicast](https://asciinema.org/a/435075.svg)](https://asciinema.org/a/435075)

## Features

- [x] Quickly browse the README of each repository
- [x] Easily clone repositories from fzf
- [x] Open URL of the repository in your default browser immediately

## Usage

```
gh fzrepo -- An extension for GitHub CLI to browse repositories with fzf

USAGE
    gh fzrepo KEYWORDS...
    gh fzrepo -h|--help
    gh fzrepo -V|--version
```

### Keybindings

| key | function |
|-----|----------|
| `Ctrl+J`, `Ctrl+N` | Move focus down |
| `Ctrl+K`, `Ctrl+P` | Move focus up |
| `Enter` | View README with `gh repo view` |
| `Ctrl+D` | Clone repository `gh repo clone` |
| `Ctrl+O` | Open URL of the repository in your default browser |
| `Esc` | Exit fzf |

## Installation

**Dependences:**

- [GitHub CLI](https://github.com/cli/cli) *v2.0.0+*
- [junegunn/fzf](https://github.com/junegunn/fzf)

```bash
gh extension install ConnerWill/gh-fzrepo
```

## One Liner Edition

```bash
query="..."; gh api "search/repositories?q=${query}" --jq ".items[].full_name" | fzf </dev/stdin	--multi	--cycle	--header "${KEYBINDINGS}" --header-first --preview "gh repo view {}" --bind "enter:execute(gh repo view {} & read && clear)" --bind "ctrl-d:execute(gh repo clone {})" --bind "ctrl-o:execute(gh repo view {} -w &>/dev/null &)" --bind "ctrl-n:change-preview-window(right,80%|up,80%,border-horizontal|hidden|right)" --bind "esc:accept-non-empty"
```

## Contribution

Welcome!

