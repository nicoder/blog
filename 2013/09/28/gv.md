# gv

In Vim's normal mode, `gv` enters visual mode in the same state as it was (same
type of visual mode, same selected area).

It is very useful because when you finish an action in visual mode, you go back
to normal mode. So if you needed to do something else in visual mode it might
be a pain to have to select the same area.

For example say I want to align the second column:

```
1  8
2 35
3 12
4 36
5  7
6 34
7  8
8 35
9 1:05
10 1:32
```

Let's say my cursor is at the beginning of the first line. I could type
`ll<Ctrl-V>jjjjjjjI <Esc>.gvjI <Esc>` and get the following result:

```
1     8
2    35
3    12
4    36
5     7
6    34
7     8
8    35
9  1:05
10 1:32
```

Here is the breakdown:

- `ll` moves to the third column, because I first want to align lines 1 to 8
with line 9
- `<Ctrl-V>` starts blockwise visual selection
- `jjjjjjj` moves down to line 8 (could have tried to do that more elegantly)
- `I <Esc>` types a space and escapes visual mode (the space is written on each of
the selected lines, in the third column)
- `.` adds another space on the same lines. At this point the first nine lines
are aligned.
- `gv` selects the same area
- `j` extends the visual selection down one line (because now we need to align
the first nine lines with the tenth).
- `I <Esc>` adds another space to the first 9 lines.
