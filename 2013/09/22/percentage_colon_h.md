# opening another file in the same directory in Vim

If I want to open a file that is in the same directory as the file in the
current window in another tab, I will often start typing this:
`:tabedit %:h/` and then the first letters of the filename followed by `<Tab>`.

`%` represents the current file name and the `:h` modifier keeps only the
directory part.

It is a bit complicated to type so I should try and use some trick to make that
easier.

Using a plugin like command-t or ctrl-p would be one way.

Gary Bernhardt has a way to simplify that. Here is the extract from his
[.vimrc](https://github.com/garybernhardt/dotfiles/blob/master/.vimrc):

```vim
""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
" OPEN FILES IN DIRECTORY OF CURRENT FILE
""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""
cnoremap %% <C-R>=expand('%:h').'/'<cr>
map <leader>e :edit %%
map <leader>v :view %%
```

I think I will try out the `%%` map.
