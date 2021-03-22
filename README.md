# woman
man-pages like cli utility for [based.cooking](https://based.cooking)

# Example Usage
## Viewing a recipe
To view a recipe:
```
$ woman Kale Banana Smoothie
```
Note that queries are case-insensitive.

You can also write a recipe to standard output instead of using a pager with the `--stdout` flag:
```
$ woman --stdout Pasta Sauce
```

## Tags and Lists
To list the names of all recipes:
```
$ woman --list
```

To list all of the tags:
```
$ woman --tags
```

Or optionally, pass a tag name to `--list` to print all of the recipes with that tag:
```
$ woman --list portuguese
```

The `--list` and `--tags` flags can be easily used to create recipe-selection menus with tools like fzf or dmenu, for example:
```
$ woman --tags | fzf | xargs woman --list
$ woman --list | dmenu -l 5 | xargs woman --stdout
```

# Tab Completion
Tab completion for recipe names is available in bash and zsh.

If you've just now installed `woman` or copied the completion files to their completion directories, you may need to restart your shell before they work.

Getting programmable completion to work for your shell in general may require additional setup in your system. If at first it doesn't work, make sure you've done the necessary setup for your distro.

# Dependencies
Install `pandoc` before using.

# Install
```
$ sudo ./install
```
Or just copy `woman` into a directory on your `$PATH` and the completion files to their respective appropriate directories.

# Uninstall
```
$ sudo ./uninstall
```

# Credits
[based.cooking](https://based.cooking) by [Luke Smith](https://lukesmith.xyz)

[Concept](https://www.youtube.com/watch?v=ykNEkiYr0QM&lc=Ugz6nFsr1PlL2x4oJaF4AaABAg) and [woman.recipes site](http://woman.recipes) by [James M](https://github.com/dm17)
