# Mark's dotfiles

## Installation

This is a collection of dotfiles and scripts I use for customizing macOS to my liking and
setting up the software development tools I use on a day-to-day basis.

## Installation

### Using Git and the bootstrap script

This repository should be cloned to your home directory so that the path is `~/dotfiles/`.
The included setup script creates symlinks from your home directory to the files which are
located in `~/dotfiles/`.

```bash
$ git clone https://github.com/hallmark/dotfiles.git ~/dotfiles
$ cd ~/dotfiles
$ source bootstrap.sh
```

To update, `cd` into your local `dotfiles` repository and then:

```bash
source bootstrap.sh
```

Alternatively, to update while avoiding the confirmation prompt:

```bash
set -- -f; source bootstrap.sh
```

## Customize

### Local Settings

The dotfiles can be easily extended to suit additional local
requirements by using the following files:

#### `~/.gitconfig.local`

If the `~/.gitconfig.local` file exists, it will be automatically
included after the configurations from [`~/.gitconfig`](git/gitconfig), thus, allowing
its content to overwrite or add to the existing `git` configurations.

**Note:** Use `~/.gitconfig.local` to store sensitive information such
as the `git` user credentials, e.g.:

```sh
[user]
  name = Mark Ture
  email = mark@example.com
```


## Sensible macOS defaults

When setting up a new Mac, you may want to set some sensible macOS defaults:

```bash
./.macos
```

## Install Homebrew formulae

When setting up a new Mac, you may want to install some common [Homebrew](https://brew.sh/) formulae (after installing Homebrew, of course):

```bash
./brew.sh
```

Some of the functionality of these dotfiles depends on formulae installed by `brew.sh`. If you don’t plan to run `brew.sh`, you should look carefully through the script and manually install any particularly important ones. A good example is Bash/Git completion: the dotfiles use a special version from Homebrew.

## Thanks to

* mathiasbynens and [his dotfiles repository](https://github.com/mathiasbynens/dotfiles)
* nicksp and [his dotfiles repository](https://github.com/nicksp/dotfiles)
