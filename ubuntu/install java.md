# Install Java

### Check if Java exists

```bash
$ sudo apt-get update
$ java -version
```

If Java is not present on the machine, choose the right version of JRE & JDK to install from the following.

### Install default JRE & JDK

```bash
$ sudo apt-get install default-jre
$ sudo apt-get install default-jdk
```

### Install default OpenJDK7

```bash
$ sudo apt-get install openjdk-7-jre
$ sudo apt-get install openjdk-7-jdk
```

### Installing Oracle JDK

```bash
$ sudo apt-get install python-software-properties
$ sudo add-apt-repository ppa:webupd8team/java
$ sudo apt-get update

$ sudo apt-get install oracle-java6-installer
OR
$ sudo apt-get install oracle-java7-installer
OR
$ sudo apt-get install oracle-java8-installer
```
