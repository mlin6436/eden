# Turn off Amazon Search Result from Dash

Dash is as helpful as Spotlight, but Amazon search is one of the features that ruin it or even Unity for me. Turning it off becomes a high priority.

### Via System Settings

As it turns out, it is really easy to do it by switching off `online search results` via `System Settings` -> `Security & Privacy` -> `Search`.

### Via Command Line

Prior to 14.04, this works sweet as a nut for me.

```bash
$ sudo apt-get remove unity-lens-shopping
```

After switching to 14.04, the command breaks my machine in a mysterious way. Also by using the easier way to turn off Amazon results by System Settings, I can only say use at your own risk.
