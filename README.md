# Dotfiles

macOS configs, managed with [GNU Stow](https://www.gnu.org/software/stow/).

## Prerequisites

```sh
brew install stow
```

## Layout

Uses stow's [`--dotfiles`](https://www.gnu.org/software/stow/manual/html_node/Invoking-Stow.html) mode (`dot-zshrc` → `~/.zshrc`).

## Install

```sh
cd ~/Dotfiles
stow .
```

## Uninstall

```sh
cd ~/Dotfiles
stow -D .
```

## Restow

```sh
cd ~/Dotfiles
stow -R .
```

## Notes

- Git identity is intentionally not in this repo. Create `~/.config/git/config.local`:

  ```ini
  [user]
    name = Your Name
    email = you@example.com
  ```

- SSH auth + commit signing via [1Password SSH agent](https://developer.1password.com/docs/ssh/) (optional).
