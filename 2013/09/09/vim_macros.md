# Vim macros

Drew Neil wrote that Vim is optimized for repetition. The 'dot' command is
great for repeating small actions. When you need something a little more
complex you reach for macros.

What is a macro? It is just a recorded sequence of keystrokes.
For example typing `qa` in normal mode will start recording a macro in register
`a`. Then all the keystrokes you type are recorded (and executed as usual)
until you type `q` which ends the recording.

Then you can execute the macro with `@a`. Or 10 times with `10@a`.
The last macro that was played can be called with `@@`.

I find macros especially useful when refactoring old code.

For example imagine we have the following javascript code:

```javascript
translations["t1"] = "translation 1";
translations["t2"] = "translation 2";
translations["t3"] = "translation 3";
```

[jshint](http://jshint.com/) tells us that it would be better to use the dot
notation.
We could use the `substitute` command with a fancy regular expression, but we
may find it easier to use a macro. Typing:

`/translations<cr>qaf[xr.f"xxnq2@a`

will turn our code into this:

```javascript
translations.t1 = "translation 1";
translations.t2 = "translation 2";
translations.t3 = "translation 3";
```

The macro keystrokes may look a bit cryptic if you are not used to Vim commands.
Here is how to break them down:
- `/translations<cr>` searches for the text "translations"
- `qa` starts the macro (and record in the 'a' register)
- `f[` finds the opening square bracket
- `xr.` deletes the bracket and replaces the double quotes by a dot
- `f"` finds the closing double-quote
- `xx` deletes the double-quote and the closing bracket
- `n` jumps to the next occurrence of the text "translations"
- `q` stops recording the macro
- `2@a` plays the macro again, twice

I like how this macro ends by positioning the cursor in the next place where
you want to execute it.

It find it often fun to carefully craft the macro in order to ensure it will be
repeatable.
