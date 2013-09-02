# Ctrl-n and Ctrl-p

Here are two autocompletion commands I use a lot in my day to day editing as a 
programmer. It often happens that I will use a variable or function name more
than once in a script (duh). Before I used Vim I would often select the word
with the mouse or keyboard, copy it, go to the place where I wanted to use it
and paste it (to avoid typos). Now in insert mode I just type the first two or
three characters of the identifier followed by `Ctrl-n` if I see the same
identifier somewhere after the place I am editing, or `Ctrl-p` if I see it
before.

(in this case think `n` for next, `p` for previous).

So it's a 'dumb' kind of automcompletion, not 'intellisense', but I find it
very useful.

From what I have experienced Vim looks for matches in the opened buffers, but
reading `:help i_CTRL-N` I see this can be configured with the 'complete'
option.

A form of autocompletion I rarely use but find pretty cool anyway is line
autocompletion.
Start typing a few characters on a line and `Ctrl-X Ctrl-L` will fill the line
to match another line starting with the same characters
See `:help i_CTRL-X_CTRL-L`.

Say I already have a line of javascript somewhere in my opened buffers that
looks like this :

```javascript
var myFunc = new function () {
```

I could type `var<Ctrl-X><Ctrl-L>` and get :

```javascript
var myFunc = new function () {
```

And then just edit the name of the function. But I never do that, and I guess
you could rather use snippets or mappings to generate this kind of boilerplate.
Or use coffeescript :)

Reading the help file shows there are tons of other stuff you can do, I should
read it more often...
