# :g

Here is a Vim command I sometimes use to quickly see a list of the functions
defined in a PHP or javascript file: `:g/function<Enter>`.

`:v/function<Enter>` does the opposite: it shows the lines that do not match
'function'. Not very useful in this case but can surely come in handy.

`:g` is a shortcut for `:global`. I used it here in a very narrow way. The
search pattern can be followed by a command that will be applied on the matched
lines. The default is `:p` ('print') which is why I see the list of functions
printed at the bottom of the window. I could have typed it
`:g/function/p<Enter>`.

Let us say there are lots of lines in a PHPCS report that I do not want to fix
right now. For example:

`4256 | WARNING | Line exceeds 120 characters; contains 126 characters`

Typing `:g/Line exceeds/d` makes those lines disappear and lets me focus on the
other coding standard violations in the list.

`:d` is an Ex command but we can also use normal mode commands with the `:normal`
Ex command. The previous command could have been typed as follows:

`:g/Line exceeds/normal dd`

In case the command produces an unexpected result: `u` will undo all the
changes at once.
