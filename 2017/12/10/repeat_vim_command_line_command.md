# Repeat a Vim command line command

For a long time, when I had a lot of opened tabs in Vim (opened with `:tabed`
or `:tabedit`)
I would either close them one by one (`:tabc` or `:tabclose`) or just keep one
tab open (with `:tabon` or `:tabonly`).

But it would sometimes happen that I wanted to close most tabs but keep two or
three open, and so I would do a lot of `:tabc`.

It turns out there is a way to repeat the last command executed on Vim's command
line: `@:`.

And it can be prefixed by a number to repeat it more than once.

Just like when executing macros, if `@:` has been called once, we can then
execute it more easily by typing `@@`.

So repeating a couple of times `4@@` allows me to close tabs way faster,
without having to count how many there are.
