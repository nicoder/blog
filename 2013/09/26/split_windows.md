# split windows

Today I watched the video of a talk Chris Hunt gave at Ancient City Ruby this
year about Vim and Tmux.

He says that he likes to focus on one thing at a time, so he likes to have only
his text file in the editor, and then only his library code, and move between
the two with `Ctrl-o` and `Ctrl-i`.

I often like to have two split windows:
- my test file on the left
- the code on the right

Sometimes I even find it useful to have two split windows displaying different
parts of the same file :)

To that effect I recently added these mappings to my vimrc:

```vim
nnoremap <leader>j <C-W><C-W><C-F><C-W><C-W>
nnoremap <leader>k <C-W><C-W><C-B><C-W><C-W>
```

So I can go one page down and own page up in the next window without leaving
the first.

Here is the breakdown :

- `<C-W><C-W>`: focus on the next window
- `<C-F>`: move down one page
- `<C-W><C-W>`: come back to the first window (this only works that way if
there are only two windows, otherwise it will cycle to a third window)

Here are some commands to deal with split windows :

- `:vs` or `Ctrl-W s`: opens the same file in a split on the left
- `:vs another_file`: opens another_file in a split on the left
- `:sp another_file`: opens another_file in a split above
- `:q` closes the current window
- `:only` or `Ctrl-W o` closes all windows except the current one
- `Ctrl-w w` moves to the next window
- `Ctrl-W j` moves to the window below
- `Ctrl-W k` moves to the window above
- `Ctrl-W h` moves to the window on the left
- `Ctrl-W l` moves to the window on the right

Lots more can be discovered in `windows.txt`.
