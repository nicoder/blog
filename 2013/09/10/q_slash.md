# q/

When you start a search in Vim with `/`, you can use the `<Up>` and `<Down>`
arrow keys (or `<Ctrl-p>` and `<Ctrl-n>`) to reuse the previous or next
searches.

It is very handy except when the search command you are looking for is far away
in the search history.

`q/` lets you see your recent search history in a buffer opened in a split
window.
You can edit a search line in the buffer if you need to and then hitting
`<Enter>` will launch the search.

The `'history'` option defines how many searches will be remembered. Its
default value is pretty low (20) but I have not yet felt the need to change it.
I see than [Ben Orenstein](https://github.com/r00k/dotfiles/blob/master/vimrc)
sets it to `500` and
[Gary Bernhardt](https://github.com/garybernhardt/dotfiles/blob/master/.vimrc)
to `10000`:)

Reading the docs, `q?` seems to do the same thing (`?` starts a search in the
opposite direction of `/`).

Similarly `q:` displays the last Ex commands in the command-line window.
