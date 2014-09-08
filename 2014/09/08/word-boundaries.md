# Word boundaries in searches

Being able to search for stuff in a file or a code base is an important skill.

A good way to remove irrelevant search results is to use word boundaries.

For example if I want to search for a variable called `f` in a file and do not
care for the variables called `from` or `foo` I could type this in Vim :

`/\<f/>`

(An easier way to do the same thing if I see an occurrence of the `f` variable
in the file would be to place my cursor on it and hit `*` in normal mode to
find the next occurrence (or `#` to see the previous occurrence)).

To do this on my whole code base from inside Vim I would do :

`:Ack "\bf\b"`

Very useful thing to know.
