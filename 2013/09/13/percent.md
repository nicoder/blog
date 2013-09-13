# %

Another very useful command in Vim's normal mode is `%`.

If the cursor is on `(` or `{` or `[` (or their closing equivalent), `%` will
make you jump to the matching parenthesis/brace/bracket.

I use it a lot to move to the end or beginning of an if/else block or function
in languages like PHP or Javacript.

I find less of a need for it in a well-factored codebase or when coding in
languages like Coffeescript or Ruby with less curly braces.

I guess it must be very useful if you are coding in Lisp, but then again maybe
in that case you would be using Emacs instead of Vim :)

`:h %` gives lots more details on how the command works and how it can be
configured.
