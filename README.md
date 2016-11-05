# The files you can use to customize [spf13-vim](https://github.com/spf13/spf13-vim)

## Installation

```
cd ~
git clone https://github.com/zzhjerry/.spf13-personal.git

# The command below will create simulinks to the files in ~/.spf13-personal/
# It is optional.
# You can also choose which file to link manually by yourself with ln -s
sh ~/.spf13-personal/configure.sh
```

## Customization rules

The settings in higher numbered files take higher precedence

1. `.vimrc.before`

Shipped with spf13-vim with some flag-like variables to control some basic behaviors.

Changes to the variables should be made in .vimrc.before.fork.

2. `.vimrc.before.fork`

Changes to the variables defined in `.vimrc.before` should be defined in this file

e.g `let g:spf13_bundle_groups=['general', 'writing', 'neocomplete', 'programming', 'python', 'javascript', 'html', 'misc']`

3. `.vimrc.before.local`

Create your own flag-like variables

4. `.vimrc.bundles`

The packages to install depending on the elements defined in `g:spf13_bundle_groups`

5. `.vimrc.bundles.fork`

Customize the bundle behaviors for default bundles (those defined in `.vimrc.bundles`)

6. `.vimrc.bundles.local`

Add new packages and configurations for them as you need.

e.g. `Bundle 'mattn/emmet-vim'`

7. `.vimrc`

The central place that controls file loading precedence, default key mappings and bundle configurations.

Understanding this file will helps you understand what spf13-vim can do for you.

8. `.vimrc.fork`

The main file to customize key mappings.

9. `.vimrc.local`

This file takes the highest precedence among all the other files.

You can put the most important settings that you don't want to be overwritten in any circumstances.

Such as your favourite color theme.
