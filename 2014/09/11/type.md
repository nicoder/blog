# type

Let us say I use an alias to ssh into my CI box and it is `sshadq`.

(it is defined this way in my .bash_profile and .zshrc :

`alias sshadq='ssh ndermine@192.168.1.28'`)

If I want to quickly see what is behind that alias I can type (no pun intended)
:

```
$ type sshadq
sshadq is an alias for ssh ndermine@192.168.1.28
```

It explains how commands would be interpreted, for example :

```
$ type git
git is /usr/local/bin/git
```

Or :

```
$ type type
type is a shell builtin
```
