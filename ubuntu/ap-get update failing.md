### apt-get update indexes not found error

This is part of the message I got when I did the normal `apt-get update`, and this stops me from being able to install ruby via rvm.

```
Err http://ppa.launchpad.net trusty/main amd64 Packages
404  Not Found
Err http://ppa.launchpad.net trusty/main i386 Packages
404  Not Found
Ign http://ppa.launchpad.net trusty/main Translation-en_GB
Ign http://ppa.launchpad.net trusty/main Translation-en
Ign http://ppa.launchpad.net trusty/main Translation-en_GB
Ign http://ppa.launchpad.net trusty/main Translation-en
W: Failed to fetch http://ppa.launchpad.net/gophers/go/ubuntu/dists/trusty/main/binary-amd64/Packages  404  Not Found

W: Failed to fetch http://ppa.launchpad.net/gophers/go/ubuntu/dists/trusty/main/binary-i386/Packages  404  Not Found

E: Some index files failed to download. They have been ignored, or old ones used instead.
```

The URLs specified don't exit anymore, which explains why I am getting this error. After some quick google, I try to `sudo apt-get update --fix-missing`, but that still doesn't  help. Then I stumble upon [this](http://blog.launchpad.net/ppa/failed-to-fetch-errors-for-ppas), and it has brighten up my day.

### Fix the missing indexes - by removing them

- Check sources list to comment out the missing indexes.

```bash
$ sudo gedit /etc/apt/sources.list
```

- Also check the sources lists in this directory, because the `gophers-go-trusty.list` I have problem with actually lives inside this folder.

```bash
$ cd /etc/apt/sources.list.d
```

### Summary

After the tweaks, I am back on business after `sudo apt-get update`.

So Why is this happening? I am using ubuntu 14.04, and the endpoints seem to have gradually been deprecated since 2011 according to [this](https://lists.launchpad.net/launchpad-users/msg06219.html), so I really don't the answer to it.
