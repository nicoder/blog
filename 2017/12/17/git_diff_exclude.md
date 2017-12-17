# Exclude files from git diff

Often I like to see the size of a diff with:
```git
git diff -w --shortstat
```

If I want to focus more on a directory I can type:
```git
git diff -w --shortstat -- that_directory
```

If I want to exclude a directory I can type:
```git
git diff -w --shortstat -- . ':(exclude)that_directory'
```

or:
```git
git diff -w --shortstat -- . ':!that_directory'
```

And if I need to exclude more than one directory:
```git
git diff -w --shortstat -- . ':!that_directory' ':!another_directory'
```

[This stack overflow question](
https://stackoverflow.com/questions/4380945/exclude-a-directory-from-git-diff
) helped me learn this.
