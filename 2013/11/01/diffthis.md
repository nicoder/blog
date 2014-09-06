# windo diffthis

I use vim a lot do see the differences between two files in a diff. Even more
so these days as I use fugitive to interact with the git repository.

If I have two windows open in splits and want to see the diff, `:windo diffthis`
will launch the diff. If I want to turn the diff off : `:windo diffoff`.

Sometimes after some changes, the diff gets out of sync, `:diffupdate` fixes
this.

Some handy commands are :
- `:diffget` or `do` to replace the current block by the corresponding block
in the other file.
- `:diffput` or `dp` to do the opposite

There are commands I always forget about that move the cursor to the next 
difference: `]c` to go to the next change and `[c` to go to the previous one.

See `:h diff` for more details.
