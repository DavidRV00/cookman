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
To list all of the available tags:
```
$ woman --tags
```

To list the names of all available recipes:
```
$ woman --list
```
Or optionally, pass `--list` a tag name to list all of the recipes with that tag:
```
$ woman --list portuguese
```

The `--tags` and `--list` flags can be easily used to create recipe-selection menus with fzf or dmenu, for example:
```
$ woman --tags | fzf | xargs woman --list
$ woman --list | dmenu -l 5 -p "Select a recipe: " | xargs woman
```

# Tab Completion
Tab completion for recipe names is available in bash and zsh.

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
