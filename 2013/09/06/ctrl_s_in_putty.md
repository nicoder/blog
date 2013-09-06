# Ctrl-S in putty

I learnt something today about putty, and about not tolerating to waste your
time at work.

In Vim I mapped `Ctrl-S` in insert mode so that it would leave insert mode and
save the current buffer :

```vim
inoremap <C-s> <Esc>:w<cr>
```

So when I program on my machine I use `Ctrl-S` all the time to leave insert
mode and save. Good. Easier than hitting `Esc`, and saving is nice.

But I sometimes use Vim in the terminal on a remote server via putty. And up
until today I would try hard to resist typing `Ctrl-S`, because when I did that
 putty would not respond any more!

So I would close putty, connect again (`windows-M`, ssh + `Enter`, wait,
username, wait ten seconds, password, `cd` to directory, recover vim file,
continue what I was doing). Not fun.

But I did that a good number of times. Way too many times. I'd usually remember
to save my files with `:w` instead of `Ctrl-S`, but every now and then the
habit would be stronger.

A couple of days ago it happened again, and I made a note in my work log to
learn how to stop `Ctrl-S` from 'freezing' my putty.

I reread the note a couple of times, and today when I hit `Ctrl-S` by accident
instead of `Ctrl-C` ìn the terminal, I finally googled `"hitting ctrl s in putty"`.
Read a blog post (the first hit :
http://raamdev.com/2007/recovering-from-ctrls-in-putty/), and immediately had
an explanation and a workaround :

`Ctrl-Q` 'unfreezes' putty.

The author (and many of the commenters) apparently also let `Ctrl-S` make him
lose time for a long period before googling it.

I once heard Gary Bernhardt say that he's not tolerant of things that will slow
him down. I should try to be less tolerant. A google search and I had the
answer in seconds. After wasting time because of my ignorance so many times
before.
