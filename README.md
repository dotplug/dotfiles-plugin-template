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

## How does it work?

The file's structure is important to handle the configuration, letting you separate each tool's configuration in different folders, allowing you to isolate each configuration.

The following structure is created by this template:

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

These folders are what we call **topics**. The structure of each topic is as follows:

- **topic/bin/**: Anything inside the bin directory will be added to the $PATH.
- **topic/install.sh**: Any file named `install.sh` will be executed automatically when plugins are being installed.
- **topic/\<FILENAME | DIRNAME>.symlink**: Any file that ends with `*.symlink` will be added as a symlink to your $HOME.

### Create a new topic

If you wanted to create a new topic you can create a directory `<TOPIC>` in the root of the plugin. Inside you can do some or all of the following:

1. Create an `install.sh` file that contains the installation process (only required for tools that are not present in Homebrew, if they are it's easier to install by updating the `Brewfile`)
2. Create an `alias.zsh` file that contains the commands you want
3. Create a file `functions.zsh` to create utility functions for that topic
4. Create a directory ending with `.symlink` that will symlink all the files inside that directory to your home directory

## How to install a plugin

If you have your plugin configured you would need to push it to your favorite repository manager. Then you can add it to ```dotfiles``` in your computer executing:

```shell
dotfiles install-plugin <GIT_REPOSITORY_URL>
```

For example:

```shell
dotfiles install-plugin git@github.com:autentia/my-awesome-plugin-template.git
```

## How to update

Plugins are linked to git repository, so you can commit your changes to your plugin repository and then execute the following command to update it:

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
