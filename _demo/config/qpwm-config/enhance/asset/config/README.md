
# Qpwm / User Config


## Subject

* [Spec](#spec)
* [User Config Dir Path](#user-config-dir-path)
* [User Config File List](#user-config-file-list)
* [Howto](#howto)
* [Test Command](#test-command)


## Spec

* [Keybind](spec-keybind.md)


## User Config Dir Path

* [~/.config/qpwm](./qpwm)

## User Config File List

run

``` sh
tree --dirsfirst ~/.config/qpwm
```

show

```
/home/user/.config/qpwm
├── bin
│   ├── qpwm-wallpaper-ctrl-default
│   └── qpwm-wallpaper-ctrl-shuf
├── style
│   ├── picom
│   │   └── picom.conf
│   └── tint2
│       └── tint2rc
├── autostart
├── environment
└── sxhkdrc

4 directories, 7 files
```




## Howto

### Install

``` sh
make install
```

### Remove

``` sh
make remove
```

## Test Command

``` sh
xmodmap -pk
```

``` sh
xev -event keyboard
```
