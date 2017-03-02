# git rebase -i / fixup

I often use `git rebase -i` to squash some commits together.

When I work, whether it is reviewing code, fixing a bug, adding a feature,
I often clean up stuff as I go, following the
[Boy scout rule](http://wiki.c2.com/?BoyScoutRule).

Sometimes these cleanups will be small independent refactoring cleanups,
but sometimes they are just many uninteresting `tidy` commits
that I will want to squash before I push them.

For that I used to use the `squash` option of `git rebase -i`.

But since it shows the commit messages of the different commits I was squashing
in my editor so I could decide which one to keep, I would always write:
- a `tidy` commit message for the first one
- and then `#tidy` for the following ones
so I could leave the commit messages untouched in the editor and git would see
them as comments.

But there is a better option in that case: `fixup`.
In that case the commits are squashed but only the first commit message is kept
(which is what I needed all along).

Now when I write a `tidy` commit message,
I do not have to care any more
whether I already have an unpushed `tidy` commit or not,
which makes my commit workflow and interactive rebase
even faster and more enjoyable.
