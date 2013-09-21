# :sort

The Vim command `:sort` will sort the lines in a range.

`:h :sort` lists some possible options.

For example, if I have this CSS declaration (taken from twitter bootstrap):

```css
.clearfix:after {
  display: table;
  content: "";
  line-height: 0;
}
```

let's say my cursor is on the selector, and I would like to sort the CSS
properties alphabetically.

Typing `jVi{:sort<Enter>` has the desired effect:

```css
.clearfix:after {
  content: "";
  display: table;
  line-height: 0;
}
```

Here is the breakdown:
- `j`: move down one line
- `Vi{`: visually select the lines in between the curly braces
-  `:sort<Enter>`: sort the lines alphabetically

`:sort!` will sort in reverse order.
