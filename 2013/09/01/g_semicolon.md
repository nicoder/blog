# g;

Here is a handy Vim command it took me some time to discover.
I would edit a part of a document, then move around in the document to look at
something, and then I would clumsily move back to where I had been editing in
the first place.

In normal mode, the `g;` command brings you back to the last cursor position in
the change list.

I opened `help g;` while writing this post and learned that you could move
quicker back in time by preceding the command with a count
(e. g. `3g;`) and also that the opposite command is `g,`
(consistent with the way you move back and forth after using `t` or `f`).

The help file also reminded me of the `:changes` Ex command.

Now I use `g;` every day.

Oh and I read on the Ruby Parley forum the other day that `gi` has a very
similar effect as `g;` : it enters insert mode at the place it was left.
Have not used it yet but it could save a keystroke I guess.
