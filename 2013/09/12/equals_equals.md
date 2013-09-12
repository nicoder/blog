# ==

In Vim's normal mode, `==` re-indents the line where your cursor is positioned.

`3==` will re-indent the line where your cursor is positioned and the two
following lines.

In visual mode `=` will re-indent the selection.

Another way I really like is to use a motion or a text-object after `=`.

For example, if I want to extract this piece of code into a method:

```php
                                $cannot = think($of);
                                $an = example($tonight);
```

(yes, PHP code buried in eight levels of indentation. Let us imagine that it is
30 lines long and also appears at 15 other places in our codebase...)

I could define my method :

```php
  public function extractedMethod($of, $tonight)
  {
  }
```

Then copy and paste the code

(for example by typing `?cannot<cr>2Yg;P`:
- `?cannot<cr>` finds the previous occurrence of `cannot`
- `2Y` copies the two lines
- `g;` moves the cursor back to the last place I edited, the closing brace of the method
- `P` pastes the two lines above the closing brace)

```php
  public function extractedMethod($of, $tonight)
  {
                                $cannot = think($of);
                                $an = example($tonight);
  }
```

And then indent it with `=i{` ("indent in between braces")

```php
  public function extractedMethod($of, $tonight)
  {
      $cannot = think($of);
      $an = example($tonight);
  }
```
