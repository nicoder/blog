# moving in the Vim command line

I have often found myself:
* with the Vim command line open (which you do by typing `:` in normal mode)
* with a pretty long command open (maybe summoned from the history by typing
the `Up` arrow a couple of times)
* wishing I could quickly move to the beginning of the line or one word at a time

But I was stuck with using the `Left` and `Right` keys.

I tried `Ctrl-A` to go to the beginning of the line, since that is how I do it
in bash, but it had no effect.

I tried `Alt-Left` to move one word to the left but again, no effect.

I had written this topic down as an idea for a blog post so today I searched
and found this
[Stack Overflow](http://stackoverflow.com/questions/2075569/how-can-i-move-around-in-the-vim-command-line)
page and finally learned a bit more.

For now I will try to remember these commands:
* `<C-b>` moves the cursor to the beginning of the Vim command line
* `<C-e>` moves the cursor to the end of the line
* `<S-Left>` moves the cursor back one word
* `<S-Right>` moves the cursor forward one word
* `<C-F>` opens the command line window, where you can find the current command
as well as the whole command history.

I had heard about the command line window (and sometimes opened  it by mistakenly
typing `q:` instead of `:q`), but I never use it on purpose, and i guess it
would sometimes be much nicer than just using the `Up` arrow.

And the same thing goes with the search history: `q/` (and `q?` if you want to
search backwards).

Read `:h cmdline-editing` for more details.
