# redirect terminal output to Vim

If the output of a shell command is very long (like a long git diff for example),
there are many ways to navigate the output directly in the terminal:
- `f` to go forward one page/screen at a time
- `b` to go back one page
- `d` to go down half a screen
- `u` to go up half a screen
- `j` to go down one line
- `k` to go up one line
- `G` to go to the end
- `g` to go to the beginning

Playing around right now it seems that `4f` moves down four lines,
`2b` moves the output up two lines.
I should try to learn more about what is available.

But sometimes you may want to have more file navigation power,
in that case you can pipe the command to Vim and read the results there:

`$ git diff -w master...develop | vim -`

I used this recently to then split the output in two windows (with `:vs`) so I
could look at different parts of the diff side by side.

I probably learnt this trick from watching
[Gary Bernhardt](https://twitter.com/garybernhardt)'s
[Destroy All Software](https://www.destroyallsoftware.com) screencasts.
