# git commit

### Edit a commit message

To edit the commit message in an [editor of choice](https://github.com/mlin6436/eden/blob/master/github/git%20configuration.md):

```bash
$ git commit --amend
```

To modify the commit message directly:

```bash
$ git commit --amend -m 'new message'
```

### Edit a commit message that has been pushed to remote branch

To edit the commit message already pushed to remote branch, simply force the change by using `--force` or `-f`:

```bash
$ git push <remote> <branch> --force
```

Or

```bash
$ git push <remote> <branch> -f
```

**Note**

- Force-pushing will overwrite the remote branch with the state of your local one.
- Be cautious about amending commits that you have already shared with other people.
