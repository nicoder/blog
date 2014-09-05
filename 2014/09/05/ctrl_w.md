# Deleting the previous word with Ctrl-W

A basic thing I (re?)learnt not that long ago : `Ctrl-W` will delete the previous
word on the command line (the word on the left of the cursor).

For example I used this a couple of times recently after tidying up some code:

I ran :
`git diff -w some/file/in/my/repo`

I saw that I could commit it in its entirety and then did :
 * `Up` (to recall the last command)
 * `Alt-Left` (to move to the beginning of the file name)
 * `Ctrl-W` twice (to remove `diff -w`)
 * then typed `add ` to obtain this command : `git add some/file/in/my/repo`
 * and finally typed `Enter` to add the file to the git index.

Before that I'd press the arrow keys a lot, this is much nicer.
