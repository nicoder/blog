# Incrementing numbers with Ctrl-A

When I learnt about this way to change numbers in Vim (I read it in Drew Neil's
_Practical Vim_ book) I did not know I would use it almost every day.

Typing `Ctrl-A` in normal mode increments the number under the cursor (or the
first number on the right if there is no number under the cursor).

`Ctrl-X` does the opposite.

`3<Ctrl-A>` adds 3 to the number.

So for example this morning while debugging a slowdown in phpunit, I wanted to 
quickly add logging statements between lines of code.

```php
self::addDirectoryContainingClassToPHPUnitFilesList('File_Iterator');
self::addDirectoryContainingClassToPHPUnitFilesList('PHP_CodeCoverage');
self::addDirectoryContainingClassToPHPUnitFilesList('PHP_Invoker');
self::addDirectoryContainingClassToPHPUnitFilesList('PHP_Timer');
self::addDirectoryContainingClassToPHPUnitFilesList('PHP_Token');
self::addDirectoryContainingClassToPHPUnitFilesList('PHPUnit_Framework_TestCase', 2);
self::addDirectoryContainingClassToPHPUnitFilesList('PHPUnit_Extensions_Database_TestCase', 2);
self::addDirectoryContainingClassToPHPUnitFilesList('PHPUnit_Framework_MockObject_Generator', 2);
self::addDirectoryContainingClassToPHPUnitFilesList('PHPUnit_Extensions_SeleniumTestCase', 2);
self::addDirectoryContainingClassToPHPUnitFilesList('PHPUnit_Extensions_Story_TestCase', 2);
self::addDirectoryContainingClassToPHPUnitFilesList('Text_Template');
```

I wrote a logging statement before the first line :

```php
logToFile("logging statement #1");
```

And then recorded the following macro : `qayyjp<C-A>q`:

- `qa` starts recording the macro
- `yy` copies the line with the #1 logging statement
- `j` moves the cursor down a row
- `p` pastes the line underneath
- `<C-A>` increments the number so we get "#2"
- `q` stops the recording

Then typing `@a` added another logging statement with the number incremented,
and with a couple of `@@` and a `5@@` I quickly got the rest of my temporary
logging statements.

```php
logToFile("logging statement #1");
self::addDirectoryContainingClassToPHPUnitFilesList('File_Iterator');
logToFile("logging statement #2");
self::addDirectoryContainingClassToPHPUnitFilesList('PHP_CodeCoverage');
logToFile("logging statement #3");
self::addDirectoryContainingClassToPHPUnitFilesList('PHP_Invoker');
logToFile("logging statement #4");
self::addDirectoryContainingClassToPHPUnitFilesList('PHP_Timer');
logToFile("logging statement #5");
self::addDirectoryContainingClassToPHPUnitFilesList('PHP_Token');
logToFile("logging statement #6");
self::addDirectoryContainingClassToPHPUnitFilesList('PHPUnit_Framework_TestCase', 2);
logToFile("logging statement #7");
self::addDirectoryContainingClassToPHPUnitFilesList('PHPUnit_Extensions_Database_TestCase', 2);
logToFile("logging statement #8");
self::addDirectoryContainingClassToPHPUnitFilesList('PHPUnit_Framework_MockObject_Generator', 2);
logToFile("logging statement #9");
self::addDirectoryContainingClassToPHPUnitFilesList('PHPUnit_Extensions_SeleniumTestCase', 2);
logToFile("logging statement #10");
self::addDirectoryContainingClassToPHPUnitFilesList('PHPUnit_Extensions_Story_TestCase', 2);
logToFile("logging statement #11");
self::addDirectoryContainingClassToPHPUnitFilesList('Text_Template');
logToFile("logging statement #12");
```

Another example: I sometimes need to add `3` to three numbers on a line. I can do
`3<Ctrl-A>`, move to the next number (or somewhere before it), type `.`, move
to (or before) the last one and type `.` again.
