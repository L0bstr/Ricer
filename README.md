# Ricer

Linux rice manager utility.

> **Status:** early planning. Nothing is implemented yet, so there is nothing to install or run.

## Why

A "rice" is a customized Linux desktop. Its config files end up scattered across `~/.config`, `/etc` and dotfiles in `$HOME`, and moving a setup to a new machine means copying them by hand and remembering which packages they need.

Ricer groups those files into self-contained **modules** (for example `waybar` or `kitty`) and manages them from one place, so a setup can be synced, applied and reinstalled without the manual work.
