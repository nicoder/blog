# J

When I learned about Vim's `J` command in normal mode, I did not think I would
use it often, but it seems I use it every day (mainly when reformatting code).

In normal mode typing `J` joins the current line and the next one.
In visual mode it will join all the selected lines.

`J` usually does the thing I want by removing the indentation whitespace in the
second line and leaving or adding just a space in between. `gJ` is another
command that joins the lines by leaving the leading whitespace untouched and
that does not add spaces.

For example, if I have one digit per line with no whitespace and my cursor on
the first line :

```
1
2
3
```

typing `3J` will produce this result :

```
1 2 3
```

while typing `3gJ` will produce this result :

```
123
```
