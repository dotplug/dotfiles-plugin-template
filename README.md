# dotfiles-plugin-template

## Getting started

This repository is used like a template by [dotfiles project](https://github.com/autentia/dotfiles). If you want to use this repository to extend your ```dotfiles``` configuration you have two options:

1. Using ```dotfiles``` command to initialize your plugin executing the following command replacing "<PLUGIN_NAME>" with the desired name:

```shell
dotfiles create-plugin <PLUGIN_NAME>
```

For example:

```shell
dotfiles create-plugin my-awesome-plugin
```


2. Fork this repository to your GitHub profile and commit your changes.


## File structure


```shell
├─ bin   # This folder contains custom binaries. 
├─ git   # This folder contains your git config.
├─ os    # This folder contains your specific config for your Operating System.
├─ zsh   # This folder contains your config scripts for your terminal.
```

Relax, you have an explanation file for each folder:

- [bin](bin/README.md)
- [git](git/README.md)
- [os](os/README.md)
- [zsh](zsh/README.md)

## How to install

If you have your plugin configured then you can add it to ```dotfiles``` in your computer executing:

```shell
dotfiles install-plugin <GIT_REPOSITORY_URL>
```

For example:

```shell
dotfiles install-plugin git@github.com:autentia/my-awesome-plugin-template.git
```

## How to update

Plugins are linked to git repository, so you can commit your changes to your plugin repository and then execute:

```shell
dotfiles update-plugin <PLUGIN_NAME>
```

For example:

```shell
dotfiles update-plugin my-awesome-plugin
```

## How to remove

If you have a plugin that you no longer want to use, you can remove it executing:

```shell
dotfiles uninstall-plugin <PLUGIN_NAME>
```

For example:

```shell
dotfiles uninstall-plugin my-awesome-plugin
```
