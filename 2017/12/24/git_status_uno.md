# Exclude untracked files from git status

Not long ago I copied a directory full of files in my git workspace to test something
and `git status` became hard to read, because all those files were listed.

I think some time ago `git status` would only list the untracked directory's name
but now it seems to list all the files.

In that case it is useful to know that:

```git
git status -uno
```

will only display the status of tracked files.

Ah, thanks to
[the git status documentation](https://git-scm.com/docs/git-status#git-status--ultmodegt)
now I see that I have this in my git config:

```
status.showuntrackedfiles=all
```

which explains the git behaviour change.

In summary:
- by default `git status` (or `git status -unormal`) only shows an untracked directory's path.
- `git status -uall` shows all untracked files
- `git status -uno` only shows tracked files
