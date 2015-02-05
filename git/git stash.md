# git stash

To stash local changes:

```bash
$ git stash
```

To see a list of stashed changes:

```bash
$ git stash list
```

To see the details of a stash:

```bash
$ git stash show # top stash changes
$ git stash show -p stash@{N} # stash N changes
```

To apply a stash back to the code, and remove it from the stash list:

```bash
$ git stash pop # pop top stash
$ git stash pop stash@{N} # pop N stash
```

To apply a stash back to the code, and keep it in the stash list:

```bash
$ git stash apply stash@{N} # apply N stash
```
