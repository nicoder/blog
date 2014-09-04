# indenting in Vim insert mode

Here is something I stumbled upon as I was reading the Vim help files while
researching yesterday's post.

When I need to change the indentation of a line (or many lines) in Vim up to
now I always did it in normal mode, with something like `>>` to have a deeper
indentation or `<<` to reduce the indentation of a line.

The `=` command in normal mode is also very helpful to correct the indentation
of some code
(for example `=i{` to reindent the body of a function delimited by braces).

But yesterday I learnt that you can also quickly indent while in insert mode :
 * `Ctrl-T` indents to the right
 * `Ctrl-D` indents to the left

I am not sure I will use that, but here is one I will certainly use : `0<C-D>`

It happens to me every now and then in old PHP code (or when I debug something
with print or log statements that I like to align all the way to the left so I
can tell at a glance that it does not belong in that code) that I would like
for a line of code to have no indentation at all.

In that case I will usually type `<<` in normal mode followed by as many `.`
commands as necessary to get to the left side of the screen (and in old PHP
code that can mean quite a few levels of indentation...).

But in insert mode you can type `0` (zero) followed by `Ctrl-D` and have the
same effect. Neat!
