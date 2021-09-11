# 🚀 gh-fzrepo

<div align="right">
    <img src="https://img.shields.io/static/v1?label=Language&message=Shell&color=blue&style=flat-square"/>
    <img src="https://img.shields.io/static/v1?label=License&message=MIT&color=blue&style=flat-square"/>
</div>

An extension for [GitHub CLI](https://github.com/cli/cli) to browse repositories with fzf

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
| `Ctrl+J`, `Ctrl+K` | move focus |
| `Ctrl+N`, `Ctrl+P` | move focus |
| `Ctrl+R` | view README with `gh repo view` |
| `Tab` | select/deselect repositories |
| `Enter` | confirm selection and open in default browser | 

## Installation

Dependences:

- [GitHub CLI](https://github.com/cli/cli) v2.0.0+
- [fzf](https://github.com/junegunn/fzf)

```bash
gh extension install sheepla/gh-fzopen
```
