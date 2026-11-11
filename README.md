# Ricer

Linux rice manager utility.

Ricer is a script utility that provides a personal organization of grouped Linux dotfiles and scripts (modules) for management functionality like install, config, etc. How things are grouped depends on the user and the creator of the module.

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
