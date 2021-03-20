# woman
man-pages like cli utility for [based.cooking](https://based.cooking)

# Example Usage
To view a recipe:
```
$ woman Kale Banana Smoothie
```
Note that queries are case-insensitive.

You can also write a recipe to standard output instead of using a pager with the `--stdout` flag:
```
$ woman --stdout Pasta Sauce
```

To list the names of all available recipes:
```
$ woman --list
```
This can be easily used to create recipe-selection menus with fzf or dmenu, for example:
```
$ woman --list | fzf | xargs woman
$ woman --list | dmenu -l 5 -p "Select a recipe: " | xargs woman
```

# Tab Completion
Tab completion is available (currently only in bash).

# Dependencies
Install `pandoc` before using.

# Install
```
$ sudo ./install
```
Or just copy `woman` into a directory on your `$PATH` and `woman-bash-completion` into `/etc/bash_completion.d`.

# Uninstall
```
$ sudo ./uninstall
```

# Credits
[based.cooking](https://based.cooking) by [Luke Smith](https://lukesmith.xyz)

[Concept](https://www.youtube.com/watch?v=ykNEkiYr0QM&lc=Ugz6nFsr1PlL2x4oJaF4AaABAg) and [woman.recipes site](http://woman.recipes) by [James M](https://github.com/dm17)
