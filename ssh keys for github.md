### Generate new ssh key

```bash
$ ssh-keygen -t rsa -C "mlin6436@gmail.com"
```

# Copy and paste the key into 'SSH Keys' in GitHub

$ cat ~/.ssh/id_rsa.pub

# Test the connection

$ ssh -T git@github.com
