# zz, zt and zb

`zz` is a command in Vim's normal mode that I often use when I want to see more
context around the line my cursor is at. That will often happen when I am
looking at different occurrences of a search.

`zz` brings the line where the cursor is to the middle of the window.

Sometimes my cursor will be at the start of a long method and I want to see as
much of the method as I can. `zt` brings the line where the cursor is to the
**top** of the window.

Conversely, if I want to see more of what happens before the line my cursor is
at, `zb` brings the cursor line to the **bottom** of the window.

`zt` => 'top', `zb` => 'bottom', `zz` => middle

Reading the help file around `:help zz` brings up interesting stuff (as
always):

- `zt`, `zz` and `zb` have near equivalents that do the same thing except they
also move the cursor to the first non blank character: `z<CR>`, `z.` and `z-`

- those commands can be prefixed by a number. For example `25zt` will place
line 25 on the top of the screen (instead of the cursor line) and move the
cursor to that line.

- typing `z20<CR>` will set the window height to 20 lines.
