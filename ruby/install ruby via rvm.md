### Intro to RVM

A full documentation on what is RVM, what it does, why uses it and a full guide on how to install it, is available [here](https://rvm.io/) and [here](https://github.com/wayneeseguin/rvm).

### Install RVM

```bash
$ \curl -sSL https://get.rvm.io | bash -s stable --rails
```

**Note** (thanks to the explanation given  [here](https://www.digitalocean.com/community/tutorials/how-to-install-ruby-on-rails-on-ubuntu-14-04-using-rvm)):

The *\curl* portion uses the *curl* web grabbing utility to grab a script file from the *rvm* website. The backslash that leads the command ensures that we are using the regular *curl* command and not any altered, aliased version.

The *-s* flag indicates that the utility should operate in silent mode, the *-S* flag overrides some of this to allow *curl* to output errors if it fails. The *-L* flag tells the utility to follow redirects.

The script is then piped directly to bash for processing. The *-s* flag indicates that the input is coming from standard in. We then specify that we want the latest stable version of *rvm*, and that we also want to install the latest stable Rails version, which will pull in the associated Ruby.

### Source RVM

```bash
$ source ~/.rvm/scripts/rvm
```

**Note**

- Type in **type rvm | head -1** and it should show **rvm is a function**, otherwise RVM hasn't been sourced correctly.

- Ensure that RVM is sourced after any path settings as RVM and manipulates the path. If you don't do this, RVM may not work as expected.

### Install a specific version of Ruby

```bash
$ rvm list known # to get a list of known ruby versions
$ rvm install ruby-head # to install a specific version of ruby
$ rvm use ruby-head # to use a specific version of ruby
```

**Note**

- On ubuntu, I bump into some problems when trying to **install ruby**, like following

```
Searching for binary rubies, this might take some time.
Checking requirements for ubuntu.
Installing requirements for ubuntu.
Updating system..................................................................................................
Error running 'requirements_debian_update_system ruby-1.9.3-p448',
please read /home/eden/.rvm/log/1379872584_ruby-1.9.3-p448/update_system.log
Requirements installation failed with status: 100.
```

To resolve this issue, refer to **ubuntu/apt-get failing**.

- On ubuntu, there could be more problem trying to **use ruby**,

```
RVM is not a function, selecting rubies with 'rvm use ...' will not work.

You need to change your terminal emulator preferences to allow login shell.
Sometimes it is required to use `/bin/bash --login` as the command.
Please visit https://rvm.io/integration/gnome-terminal/ for an example.
```

This can be fixed by going into *Preference* -> *Title and Command*, and tick *Run command as a login shell*.

### Summary

Until now, I have a working version of Ruby managed by RVM.