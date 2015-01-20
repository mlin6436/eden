# Passwordless Login

### Copy RSA key to the target remote machine

```bash
$ cat ~/.ssh/id_rsa.pub | ssh <user>@<ip> 'cat >> ~/.ssh/authorized_keys'
```

### Set up alias for quick access

```bash
$ echo "alias apple='ssh <user>@<ip>'" >> ~/.bashrc # Or `.bash_profile` on Mac
```
