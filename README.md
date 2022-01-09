<div align="center">

<img width="400" height="400" src="https://asciinema.org/a/435075.svg">

# rocket gh-fzrepo

### **Browse and clone repositories with fzf**
> An extension for [GitHub CLI](https://github.com/cli/cli) to browse and clone repositories with fzf.

![GitHub last commit](https://img.shields.io/github/last-commit/ConnerWill/gh-fzrepo)
![GitHub issues](https://img.shields.io/github/issues-raw/ConnerWill/gh-fzrepo)
![GitHub repo size](https://img.shields.io/github/repo-size/ConnerWill/gh-fzrepo)
[![GitLab](https://img.shields.io/static/v1?label=gitlab&logo=gitlab&color=E24329&message=mirrored)](https://gitlab.com/ConnerWill/gh-fzrepo)
![GitHub](https://img.shields.io/github/license/ConnerWill/gh-fzrepo)
![GitHub Repo stars](https://img.shields.io/github/stars/ConnerWill/gh-fzrepo?style=social)

---
</div>


# Features

- [x] Quickly browse the README of each repository
- [x] Easily clone repositories from fzf
- [x] Open URL of the repository in your default browser immediately

---

# Table of Contents

<details>
  <summary>Table of Contents</summary>

* [^=^z^` gh-fzrepo](#z-gh-fzrepo)
* [Features](#features)
* [Table of Contents](#table-of-contents)
* [Usage](#usage)
   * [Keybindings](#keybindings)
   * [Installation](#installation)
   * [One Liner Edition](#one-liner-edition)
* [Contribution](#contribution)

</details>

# Usage

```bash
gh fzrepo <SEARCH>
gh fzrepo -h|--help
gh fzrepo -V|--version
```

## Keybindings

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

---

## One Liner Edition

```bash
query="..."; gh api "search/repositories?q=${query}" --jq ".items[].full_name" | fzf </dev/stdin    --mu>
```

# Contribution

Welcome!

---
