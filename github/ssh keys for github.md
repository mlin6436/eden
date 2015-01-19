# SSH keys for GitHub

### Generate new ssh key

```bash
$ ssh-keygen -t rsa -C "mlin6436@gmail.com"
```

### Copy and paste the key into 'SSH Keys' in GitHub

```bash
$ cat ~/.ssh/id_rsa.pub
```

### Test the connection

```bash
$ ssh -T git@github.com
```
