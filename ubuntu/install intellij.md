# Install IntelliJ

### Download IntelliJ

Download IntelliJ source package from [JetBrains](https://www.jetbrains.com/idea/download/)

### Unzip the package, then Rock'n'Roll

```bash
$ tar -xvf <idea*.tar.gz>
```

If you don't mind a bit of messiness, use the following command to get cracking. Otherwise, carry on reading if you'd like things organised.

```bash
$ cd idea/bin
$ ./idea.sh
```

### Move IntelliJ to a central location

```bash
$ sudo mv idea /usr/share/
```

### Launch IntelliJ via Terminal

```bash
$ cd /usr/bin/
$ sudo ln -s /usr/share/idea/bin/idea.sh idea
$ idea $
```

### Launch IntelliJ via Custom Launcher

To use a more native approach to launch IntelliJ, create a custom launcher for it. Follow the instructions in [Custom launcher in Ubuntu](https://github.com/mlin6436/eden/blob/master/ubuntu/custom%20launcher%20in%20ubuntu.md).
