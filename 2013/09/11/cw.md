# cw

Here is another command I often use in Vim: `cw`. In my head I read it as
'change word', even if it does not do exactly that.
It does that, more or less, if my cursor is on the first character of the word.
If the cursor is somewhere inside the word, it will delete the end of the word
and place me in insert mode.

I will often use that in combination with a search to rename a variable in more
than one place.

For example, if I have a variable named `notSureHowToCallThisVariable` in the
following code:

```javascript
var notSureHowToCallThisVariable = resultOfSomeCalculation();
notSureHowToCallThisVariable += someOtherCalculation();
return notSureHowToCallThisVariable;
```

Let us say I decide the variable would be better named `foobinator`, and let us
say that my cursor is on the first variable. I could type:

`*cwfoobinator<Esc>n.n.`

and get the following result:

```javascript
var foobinator = resultOfSomeCalculation();
foobinator += someOtherCalculation();
return foobinator;
```

- `*`: go to the beginning of the next occurrence of `notSureHowToCallThisVariable`
- `cwfoobinator`: change the variable name to `foobinator`
- `<Esc>`: leave insert mode / go back to normal mode
- `n`: go to the next occurrence
- `.`: repeat the substitution
- `n.`: go to the last occurrence and repeat the substitution

I love how you do the work once and then `n.` does the same thing as many times
as you want.

If the cursor is in the middle of the word you could use `ciw` or `caw` or
`ciW` or `caW`.

Some other very useful variations:`ci(` (change inside parentheses) and `ci"`
(change inside quotes).
