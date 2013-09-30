# *

In Vim's normal mode, `*` moves the cursor to the next occurrence of the word.

`#` does the same thing in the opposite direction.

Then (as when you search with `/`) `n` moves to the next occurrence and `N` to
the previous one.

Very very useful. For example to see the uses of a variable or function in a
file without having to type it in a search.

And it's taught me the syntax of word delimiters in Vim.
If you use `*` on the word `Vim` and then type `/<Up>` to bring up the last
search that was executed, you will see this in the command line at the bottom
of the screen:

`/\<Vim\>`

- `\<` marks the beginning of a word
- `\>` marks the end of a word
