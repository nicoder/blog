# start insert mode with I and A

In Vim's normal mode `I` starts insert mode before the first non-blank character.

So for example if I want to comment three lines of code and my cursor is on the
first line, it does not matter in which column the cursor is, I can just type
`I//<Esc>j.j.` and this code 

```javascript
  one();
  two();
  buckleMyShoe();
```

becomes

```javascript
  //one();
  //two();
  //buckleMyShoe();
```

Here is the breakdown:
- `I` starts insert mode before `one()`
- `//` comments the line
- `<Esc>` leaves insert mode, back to normal mode
- `j` moves down to the next line
- `.` repeats the text insertion
- `j` moves down to the next line
- `.` repeats the text insertion

We do not have to move explicitly to the first non blank character, which makes
the command more repeatable.

Similarly `A` starts insert mode at the end of the line.

`I` is a shortcut for `^i`.
`A` is a shortcut for `$a`.
