# G and gg

Another two motion commands I use a lot :
- `G` moves to the end of the file
- `gg` moves to the beginning of the file

`15G` moves to line 15 of the file.

`:15<Enter>` does the same thing and I used to do it like that, but `15G` is
one less keystroke.

Reading `h gg` I learnt that `15gg` also moves to line 15 of the file.
And that it moves to the first non blank character of the line (as does `15G`).

As with other motion commands, this is useful when combined with an action.

For example `dG` will delete till the end of the file.
`dgg` will delete till the beginning of the file.
