# bashlock

bash script to lock the console.

It requires the password of the calling user to unlock the console. This utility is similar in spirit to `vlock`, the only reason it exists is because `vlock` was unavailable for OS X.

The main purpose of `bashlock` is to be used as a `lock-server` inside `tmux`. This allow you the user to lock `tmux` sessions.

### Dependencies

`bashlock` has very few dependencies, namely:

- bash
- expect
- su

Recent versions of OS X (>= 11.9) have all dependencies pre-installed.

Respectable linux distributions provide `bash` and `su` pre-installed, and in debian-based systems you can install expect via `sudo apt-get install expect`.

To install simply copy somewhere in your path, the recommended location
is `/usr/bin`.


### Usage in tmux

Assuming `bashlock` is in your `$PATH`, placing the following in your
`~/.tmux.conf` file will bind the shortcut `Meta-X` to lock tmux.

```
# Screen lock
bind-key -n M-x lock-server
set-option -g   lock-after-time 0
set-option -g   lock-server on
set-option -g   lock-command "bashlock"
```
