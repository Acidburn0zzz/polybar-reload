# polybar-reload

Signals `polybar` to reload when screen resolution has changed. Especially useful
when running in a vm, when screen resizes can occur often.

Currently supports one screen.

## Installation

Enable interprocess communication for each bar you would like to reload:

Edit `~/.config/polybar/config`:

```
[bar/myBar1]
enable-ipc = true
...


[bar/myBar2]
enable-ipc = true
```

Install `polybar-reload`:

`pip install --user polybar-reload`


Run `polybar-reload`. This can be done in a number of places. If you don't use
any of the tools mentioned below, you can run `polybar-reload` in whatever script
you use to start polybar.

### for i3 users:

`~/.config/i3/config`

```
exec --no-startup-id polybar-reload
```

This will load polybar on startup, but not on "reload i3" (commonly bound to Mod+Shift+r)

## Upgrading

`pip install --upgrade --user polybar-reload`
