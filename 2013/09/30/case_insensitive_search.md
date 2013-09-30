# case insensitive search

I had to look this up again today. By default, Vim does case sensitive search.
So if I search `/vim` I will not find the first occurrence : `Vim`.

If I want a case insensitive search i need to add `\c` somewhere in the search
command. So if I search for `/vim\c` or `/\cvim`, I will also find `Vim`.

I like having case sensitive search by default.

If you prefer case insensitive by default, you can type `:set ignorecase`.

In that case `/vim` matches both `vim` and `Vim`.

There is a similar way to ask for case sensitivity in that case : `/vim\C` will
match only `vim`.

Finally when `ignorecase` is set, `:set smartcase` does case-insensitive search
if the search pattern is in lowercase, but case sensitive if it contains an
uppercase letter.
