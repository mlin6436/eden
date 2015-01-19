# Install Spotify

Thanks to [spotify](https://www.spotify.com/uk/download/previews/), installing spotify on Debian/Ubuntu is easy:

### Add spotify source `deb http://repository.spotify.com stable non-free` to the list of repositories

```bash
$ sudo vi /etc/apt/sources.list
```

### Add public key to verify the downloaded packages

```bash
$ sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 94558F59
```

### Run apt-get update

```bash
sudo apt-get update
```

### Install spotify

```bash
sudo apt-get install spotify-client
```
