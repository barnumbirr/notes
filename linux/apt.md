# APT

## Replicate packages installed from one host to another

On the source machine:

```bash
$ apt-get update && apt-get dist-upgrade
$ cat /etc/apt/sources.list /etc/apt/sources.list.d/* > sources.list
$ dpkg --get-selections > selections.list
$ apt-mark auto > auto.list
```

On the target machine:

```bash
$ cp sources.list /etc/apt/
$ apt-get update
$ dpkg --set-selections < selections.list
$ apt-get dselect-upgrade
$ xargs apt-mark auto < auto.list
```
