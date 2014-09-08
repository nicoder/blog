# Ctrl-U

In an Unix shell it sometimes happens that I start writing a command then
change my mind and decide I want to execute something else instead.

In that case I would usually either delete everything with one `Backspace` key
per character (not very efficient) or `Ctrl-C` to get a new prompt (but the not
executed command would still be on the screen).

I think I learnt about 'Ctrl-U' in this article :
http://www.skorks.com/2009/09/bash-shortcuts-for-maximum-productivity/

In my shell it deletes the whole line because I am using zsh.
In bash it deletes from the cursor position to the beginning of the line.

In both bash and zsh `Ctrl-K` deletes from the cursor to the end of the line.

And when you deleted something this way, you can later paste it with `Ctrl-Y`.
