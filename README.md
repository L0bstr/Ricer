# Ricer

Linux rice manager utility.

> **Status:** early planning. Nothing is implemented yet, so there is nothing to install or run.

## Why

A "rice" is a customized Linux desktop. Its config files end up scattered across `~/.config`, `/etc` and dotfiles in `$HOME`, and moving a setup to a new machine means copying them by hand and remembering which packages they need.

Ricer groups those files into self-contained **modules** (for example `waybar` or `kitty`) and manages them from one place, so a setup can be synced, applied and reinstalled without the manual work.

## Concept

```
  System files                  Ricer modules
  ------------                  -------------
  ~/.config/waybar/   <--+--->  modules/waybar/files/
  ~/.config/kitty/    <--+--->  modules/kitty/files/
  ~/.zshrc            <--+--->  modules/zsh/files/
                         |
                  sync (system -> module)
                  apply (module -> system)
```

## Commands

| Command   | What it will do                                  | Status  |
|-----------|--------------------------------------------------|---------|
| `module`  | Create and manage modules                        | planned |
| `sync`    | Copy current system files into a module          | planned |
| `apply`   | Put a module's files in place on the system      | planned |
| `install` | Install the packages and deps a module needs     | planned |
| `run`     | Run a module's setup steps                       | planned |

## Module layout (planned)

Layout is a draft and may change as the tool takes shape.

```
modules/
└── waybar/
    ├── files/        # config files, mirroring their system paths
    ├── manifest      # where each file goes, plus metadata
    ├── install.sh    # installs packages the module needs
    └── setup.sh      # post-apply steps (reload, enable services)
```

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) (coming soon).
