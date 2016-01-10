# git commit --verbose

I don't remember where I heard about this, but -

Ok, googling "nicoder verbose" refreshed my memory:
I learned about `git commit --verbose` because
[Tom Stuart](https://twitter.com/tomstuart) mentioned it in a
[tweet](https://twitter.com/tomstuart/status/661127211458674688).

If you add this flag, the diff of what you are commiting will appear at the
end of the file you write your commit message in.

I find it really nice for:
* checking what I am commiting one last time, even if I usually use `git add -p`
and `git diff --staged` (aliased to `git ds`)
* having more autocompletion in Vim with `Ctrl-n` and `Ctrl-p`.

It can be abbreviated to `git commit -v`.

The [docs](https://www.kernel.org/pub/software/scm/git/docs/git-commit.html)
also say "If specified twice, show in addition the unified diff between what
would be committed and the worktree files, i.e. the unstaged changes to tracked
files.",
but I tried `git commit -v -v` with only a part of my changes to tracked files
staged and did not notice a difference.
