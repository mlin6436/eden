# Install Atom

### Install Atom via PPA

Thanks to [webupd8](http://www.webupd8.org/2014/05/install-atom-text-editor-in-ubuntu-via-ppa.html), Atom can be easily installed via the PPA they provided.

```bash
$ sudo add-apt-repository ppa:webupd8team/atom
$ sudo apt-get update
$ sudo apt-get install atom
```

```bash
$ sudo apt-get remove atom
$ sudo add-apt-repository --remove ppa:webupd8team/atom
$ sudo apt-get autoremove
```

### Install Atom via .deb

Using PPA to install atom has worked for me quite happily until recently, either because of a problematic PPA portal or a broken release webupd8 put online. Anywhere, I fall back to the last resort: the [offical channel](https://github.com/atom/atom), and surprisingly, the installation process seemed easy enough.

- Down `atom-amd64.deb` from [Atom releases page](https://github.com/atom/atom/releases/tag/v0.166.0).
- Run `sudo dpkg --install atom-amd64.deb` on the downloaded package.
- Launch Atom using the installed `atom` command.
