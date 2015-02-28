# git stage

### Bulk stage deleted files

```bash
$ git ls-files --deleted -z | xargs -0 git rm
```

The previous version works for me, but try the following version (which doesn't work for me) out as it looks more compact.

```bash
$ git rm $(git ls-files --deleted)
```
