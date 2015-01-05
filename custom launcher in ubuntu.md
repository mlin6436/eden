### Create a launcher file

```bash
$ cd /usr/share/applications
```

```bash
$ sudo vi <applicaiton>.desktop
```

### Use the application content template
```text
[Desktop Entry]
Name=IntelliJ IDEA
Comment=IntelliJ IDEA
Exec=/usr/share/idea/bin/idea.sh
Icon=/usr/share/idea/bin/idea.png
StartupNotify=true
Type=Application
```
