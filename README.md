This is based on https://github.com/vysheng/tg/wiki/User-level-daemon-on-Arch-linux-with-systemd

The files included in this repository are used to run hourly telegram backups via systemd.

# Requirements

* [telegram-cli](https://github.com/vysheng/tg)
* [telegram-history-dump](https://github.com/tvdstaaij/telegram-history-dump)

# Installation

Copy all files to

```
~/.config/systemd/user
```

# Usage

Enable and start the telegram-cli service:

```
systemctl --user enable telegram-cli
systemctl --user start telegram-cli
```

Enable and start the telegram-history-dump timer:

```
systemctl --user enable telegram-history-dump@username.timer
systemctl --user start telegram-history-dump@username.timer
```

Where _username_ is your local user name.
