# Disable Guest Session

```bash
$ sudo vi /usr/share/lightdm/lightdm.conf.d/50-ubuntu.conf
```

Add the following line to the file:

```text
allow-guest=false
```

Reboot the system and see the guest session gone.
