# bashlock

bash script to lock the console.

It requires the password of the calling user to unlock the console. This utility is similar in spirit to `vlock`, the only reason it exists is because `vlock` was unavailable for OS X.

The main purpose of `bashlock` is to be used as a `lock-server` inside `tmux`. This allow you the user to lock `tmux` sessions.

### Dependencies

`bashlock` has very few dependencies, namely:

- bash
- expect
- su

Recent versions of OS X (>= 10.9) come with all the above utilities installed by default. 

All respectable linux distributions provide `bash` and `su` preinstalled, and in debian-based systems you can install expect via `sudo apt-get install expect`.
