# move to next paragraph

In Vim's normal mode, `}` moves to the next paragraph, `{` to the previous one.

If I have small methods in a class without empty lines in them and separated by
an empty line, `}` will lead me to the end of the method.

So for example if I want to copy and paste a test method:

```php
    public function testSomething()
    {
        givenWeHaveSomething();
        whenWeDoSomething();
        thenWeShouldSeeThis();
    }

    public function anotherTest()
    {
```

If my cursor is on the line where the method name is, I could duplicate it with
`V}y}p` and get the following result:

```php
    public function testSomething()
    {
        givenWeHaveSomething();
        whenWeDoSomething();
        thenWeShouldSeeThis();
    }

    public function testSomething()
    {
        givenWeHaveSomething();
        whenWeDoSomething();
        thenWeShouldSeeThis();
    }

    public function anotherTest()
    {
```

- `V` starts linewise visual mode, so I can see what will be selected
- `}` moves to the empty line after the method (so the whole method is visually
selected)
- `y` yanks (copies) the selection and goes back to normal mode. The cursor is still on the first line.
- `}` moves to the empty line after the method
- `p` pastes the method below

Similarly, if you are editing text, `)` and `(` move to the next/previous
sentences. As with most commands, they can be prefixed with a count, so `4(`
will move the cursor back 4 sentences.
