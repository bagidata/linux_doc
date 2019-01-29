## Modifikasi tampilan terminal bash


```
user@hostname:~$ PS1="${debian_chroot:+($debian_chroot)}[\[\e[0;32m\]\u@\H, load: `cat /proc/loadavg | awk '{ print $1; }'`\[\e[00m\]] (\[\e[00;35m\]\d - \t\[\e[00m\])\n\w \$ "
[user@hostname, load: 1.25] (Sel Jan 29 - 23:05:48)
~ $ echo $PS1
[\[\e[0;32m\]\u@\H, load: 1.25\[\e[00m\]] (\[\e[00;35m\]\d - \t\[\e[00m\])\n\w $
[user@hostname, load: 1.25] (Sel Jan 29 - 23:21:21)
~ $ echo "export \$PS1='$PS1'" >> ~/.bash_profile
[user@hostname, load: 1.25] (Sel Jan 29 - 23:22:39)
~ $ 

```
