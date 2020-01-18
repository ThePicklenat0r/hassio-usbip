# USB-Over-IP

A USB-over-IP client for Hass.io

## Warning

This addon is experimental and does not work; it probably never will.

## About

A USB-over-IP client to extend USB devices over your network (such as a z-stick)
into your Hass.io instance.

**NOTE:** _Requires the companion usbip-server somewhere on your network._

## How to use

This addon is not published to the repository and needs to be built locally from /addons

## Configuration

**Note**: _Remember to restart the add-on when the configuration is changed._

Example add-on configuration:

```json
{
  "log_level": "info",
  "server": "192.168.1.5:8888",
  "devId": "ttyZWAVE"
}
```

### Option: `log_level`

The `log_level` option controls the level of log output by the addon and can
be changed to be more or less verbose, which might be useful when you are
dealing with an unknown issue. Possible values are:

- `trace`: Show every detail, like all called internal functions.
- `debug`: Shows detailed debug information.
- `info`: Normal (usually) interesting events.
- `warning`: Exceptional occurrences that are not errors.
- `error`:  Runtime errors that do not require immediate action.
- `fatal`: Something went terribly wrong. Add-on becomes unusable.

Please note that each level automatically includes log messages from a
more severe level, e.g., `debug` also shows `info` messages. By default,
the `log_level` is set to `info`, which is the recommended setting unless
you are troubleshooting.

### Option: `server`

The IPv4 address of the USB-over-IP server.

### Option: `devId`

Where to map the device in /dev

**NOTE:** _Currently, only one device can be attached._

[community-example]: https://github.com/hassio-addons/addon-example
