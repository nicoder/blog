# ctrlp shortcuts

I have been using [ctrlp](https://github.com/ctrlpvim/ctrlp.vim) to help me
fuzzy search files to open in Vim for a long time.

But I usually used it this way:

```
:tabed(it) # to open a new Vim tab
,f         # to open ctrlp (it is mapped this way in my `~/.vimrc`:
           # `nnoremap <leader>f :CtrlP<cr>`)
ABCFilter  # to locate the file (the file path must contain the letters in that
           # order, but they do not have to be consecutive)
Enter      # to open the file in the tab I opened earlier
```

I started reading Drew Neil's
[Modern Vim](https://pragprog.com/book/modvim/modern-vim) book recently,
and he writes a little about FZF, another fuzzy file searcher.

That made me realize that I could use ctrlp in a more efficient manner.

For example to find a file and open it in another tab I can do:

```
,f        # to open ctrlp
ABCFilter # to locate the file
Ctrl-t    # to open the file in a new tab
```

`Ctrl-v` and `Ctrl-x` can be used to open the file in (vertical or horizontal)
splits instead.

Another workflow that can be simplified is opening a file and its test file.

I used to do :

```
:tabed(it)    # to open a new Vim tab
,f            # to open ctrlp
ABCFilter     # to locate the file
Enter         # to open the file in the tab I opened earlier
:vs           # or `:vsplit` to split the screen in two windows
,f            # to open ctrlp again
ABCFilterTest # to locate the test file
Enter         # to open the test file in the new split window
```

By using `Ctrl-z` to mark multiple files and `Ctrl-o` to open them this becomes:

```
:tabed(it) # to open a new Vim tab
,f         # to open ctrlp
ABCFilter  # to locate the file and the test file
Ctrl-z     # to mark one file
Ctrl-k     # (or arrow Up) to move up to the next file
Ctrl-z     # to mark the other file
Ctrl-o     # to open both files in split windows
```

Also if we type for example `:42` at the end of the text search
the file will be opened at line 42.

There is a thing to be said about reading the docs of our tools and wondering
if we could use them in a more efficient manner :)
