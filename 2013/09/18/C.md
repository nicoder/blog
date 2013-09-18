# C

Another command I use pretty frequently in Vim's normal mode is `C`.
It deletes everything from the cursor to the end of the line and starts insert
mode. It is the equivalent of `c$`.

For example if I want to change the following `else if` clause into an `else`
and my cursor is at the beginning of the line, I can type: `fiC{<Esc>`.

```javascript
} else if (blaBlaBla()) {
```

the code will become:

```javascript
} else {
```

Reading `:h C` I learnt that if you do `2C` it will delete the end of the line
and the following line before starting insert mode.

The text that was deleted is stored in a register, so `p` will paste it back.
If you need another register than the default one you can specify it with `"bC`
for example and then you can paste it with `"bp`.
I almost never use those registers in that way but I will keep an eye out for
opportunities to use them (and I just used a `2C` (which I had never used
before) to edit this sentence :)).
