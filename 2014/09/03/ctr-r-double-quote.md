# Ctrl-R + "

Another thing in Vim I can't seem to remember :
sometimes I'd like to yank (copy) a word in my Vim buffer and then paste it in
the Vim command line.

For example I'm at the beginning of a long class name, in visual mode, and I'd
like to see where it is used in the project.

I'll type `yw` to copy the class name. Then `:Ack ` to start doing my search,
and then I will usually type the whole class name because I forgot how to paste
in the Vim command line.

It happened to me again today and for maybe the tenth timed I googled 'paste in
the Vim command line' and found the solution : `<c-r>"` (Control-R followed by
a double quote).

Hopefully now that I have written this small post I will remember.

The same keystrokes can be used in insert mode, I never use them but it could
come in handy, I should keep an eye out.

`:h i_CTRL-R` tells us way more about this. `Ctrl-R` can be followed by any
register, and `"` contains the last yanked text.

Oh, `<c-r>%` inserts the name of the current file! (another thing I know I read
about but never remember ; and I know I need it every now and then).

`<c-r>/` inserts the last search pattern, pretty cool.

I'm not going to paraphrase the rest of the help entry but it is pretty
interesting what you can do with `<c-r>.`, `<c-r>-` or `<c-r>=`.
