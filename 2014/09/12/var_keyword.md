# the var keyword (in JavaScript)

I always read that it is very important when writing JavaScript to use the
`var` keyword when defining variables that you only need inside a function.

```
function aFunction() {
    var first, second, third;
    [...]
}
```

Otherwise they are automatically global variables.

I more or less understood that it could cause problems and usually remember to
use the `var` keyword but I finally encountered a bug in our system because of
that.

We have a global function called `url` and another function did something like
this :

```
function someFunction() {

    url = '/some/url'; // <---- ooh, no `var` keyword :-(

    $.get(url, [...], function() {
        doSomethingWhenTheAjaxCallReturns();
    });
}
```

It turns out that by assigning a value to `url` without using the keyword `var`
the global `url` function was not a function any more, so later code that
called `url(...)` would result in a JavaScript error because `url` had become a
string.

Another lesson is that having a global function named `url` is risky, it would
be better to namespace it, at least.
