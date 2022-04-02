
# Boot

## Subject

* [Xsession](#xsession)
* [Autostart](#autostart)
* [Howto](#howto)


## Xsession

| Path | Note |
| --- | --- |
| [/usr/share/xsessions/qpwm-session.desktop](xsessions/qpwm-session.desktop) | start here |
| [/usr/share/qpwm/xsessions/qpwm-session](xsessions/qpwm-session) | qpwm-session.desktop call this script |


## Autostart

> Not using system wild if user file exists.

### System Wild

| Path |
| --- |
| [/usr/share/qpwm/config/qpwm/environment](config/qpwm/environment) |
| [/usr/share/qpwm/config/qpwm/autostart](config/qpwm/autostart) |


### Per User

| Path |
| --- |
| [~/.config/qpwm/environment](../config/qpwm/environment) |
| [~/.config/qpwm/autostart](../config/qpwm/autostart) |


## Howto

### Install

``` sh
make install
```

### Remove

``` sh
make remove
```
