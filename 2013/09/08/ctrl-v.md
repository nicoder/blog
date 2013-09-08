# Ctrl-V

There are three visual modes in Vim, `v` starts characterwise visual mode (i.e. 
you can select characters of one ore more lines, `V` starts linewise visual
mode (select whole lines), and `Ctrl-V` starts blockwise visual mode.

I use `v` and `V` mainly for selecting sections to copy or cut.

`Ctrl-v` makes it possible to do the same editing on more than one line at
once, on a rectangular block of code.

For example if I want to delete unwanted spaces in this javascript object:

```javascript
a = {
    a1:   1,
    a2:   2,
    a3:   3
};
```

I could place my cursor after the first colon and do `Ctrl-Vjjx.`

```javascript
a = {
    a1: 1,
    a2: 2,
    a3: 3
};
```

`Ctrl-V` enters visual block mode, `jj` selects the first space on the two 
lines under the first one, `x` will delete those three spaces at once (and exit
visual mode), and `.` repeats the command, so the following three spaces are
deleted.

A nice command to know is `gv`: it will re-select the last thing that was
selected in visual mode.

Another nice thing: if I messed up my `Ctrl-v` and hit `Vjj` instead, I end
up in linewise block mode with more characters selected than I wanted.
Hitting `Ctrl-V` will correct that and place me in block visual mode.
