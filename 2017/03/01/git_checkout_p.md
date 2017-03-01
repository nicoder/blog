# git checkout -p

I often use `git checkout -p` to remove debugging statements I temporarily
added to my code.

Juste like `git add -p` or `git reset -p`, git will show me the different
changes I made and I can choose which ones to keep and which ones to discard.

A few days ago I almost had a little misadventure with this command.
I had a bunch of changes and wanted to:
* discard some temporary changes
* make some commits with the rest of the changes.

I ran `git checkout -p` to start by deleting the temporary changes that I did
not want to keep.

But midway through I forgot what I was doing and wrongly marked for deletion
stuff I wanted to add to a commit...

Once things are commited in git, there should always be a way to recover from a
wrong command.
But git cannot help you if you do an error like this before commiting.

Luckily I still had the file open in Vim,
so I could juste force save the file and did not lose any work.

So from now on I think I'll try to make my commits first,
and remove unwanted changes with `git checkout -p` at the end.
Or just be extra careful.

In that case I could just use `git reset --hard`,
but just as I like using `git add -p` even when I know that I want to add all
my changes,
`git checkout -p` allows me to verify each change once more, one by one.
