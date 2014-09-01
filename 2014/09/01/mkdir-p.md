# mkdir -p

Here is another command option that i never remember
(but then `man mkdir` gives the answer even faster than Google) :

If I try to create a directory on the Unix command line and an intermediary directory does not exist, I get an error :

```
$ mkdir a/b/c
mkdir: a/b: No such file or directory
```

The `-p` flag tells `mkdir` to create the intermediary directories if they do not exist :

```
$ mkdir -p a/b/c
$ ls -al a/b/c
total 0
drwxr-xr-x  2 nico  staff   68 Sep  1 17:16 .
drwxr-xr-x  3 nico  staff  102 Sep  1 17:16 ..
```
