To start with, Git will look for `/etc/gitconfig` to retrieve custom settings for all users on the target machine. Secondly, Git will look up `~/.gitconfig` or `~/.config/git/config` for settings specific to an individual user.

Here is a list of things to do when first setting up Git:

### Update name and email address:

```bash
$ git config --global user.name "Meng Lin"
$ git config --global user.email mlin6436@gmail.com
```

### Change editor to one's choice:

To edit the commit message already pushed to remote branch, simply force the change by using `--force` or `-f`:

```bash
$ git config --global core.editor vim
```

### Use a template for commit message:

```bash
$ git config --global commit.template ~/.gitmessage.txt
```

The template `~/.gitmessage.txt` would have something like:

```message
[ticket: X]

what's been done
```

**Note**

If in doubt, always use `man git-config` to find a comprehensive description of all settings available.
