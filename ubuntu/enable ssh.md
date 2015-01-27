# Enable SSH

In order to [SSH](http://en.wikipedia.org/wiki/Secure_Shell) into an Ubuntu box, `openssh-server` needs to be installed.

```bash
$ sudo apt-get install openssh-server
```

If for any reason a different port (instead of default port 22) is required for accessing the box, it can be done by editing

```bash
$ sudo vi /etc/ssh/sshd_config
```

with the following line

```text
Port 22
```

To connect to the box, use command

```bash
$ ssh <user>@<ip_addr> -p <port_number>
```
