# Ctrl-Z / fg

A nice thing I learnt watching Gary Bernhardt's Destroy All Software
screencasts :
when you're inside vim in the terminal, you can return briefly to the terminal
with `Ctrl-Z` : it does not close vim, it just suspends its execution and puts
it in the background.

Then you can do what you have to do in the terminal, and then you can come back
to where you were in vim with `fg`.

Nowadays I don't use it that much because I'll use different windows in tmux
for my editor and my terminal but it comes in handy once in a while when I am
debugging something on a remote server.

In doing some research for this post, I see that you can type `jobs` in the
terminal to see the background jobs, and then you can reach them by number,
for example `fg %1`.

Oh, and I see how that ties up with running commands suffixed by `&`, which
makes the job run in the background. I can then see which ones are running with 
`jobs` and kill them if necessary with for example `kill %2`.

Just tried that in a terminal where I had launched the git GUI with `gitk &`,
fun!

Some pages I found helpful :
 * http://www.thegeekstuff.com/2010/05/unix-background-job/
 * http://docs.jach.hawaii.edu/JAC/JACUN/008.0/node47.html
 * http://superuser.com/questions/476873/what-is-effect-of-ctrl-z-on-a-unix-linux-application
 * http://en.wikipedia.org/wiki/Control-Z
