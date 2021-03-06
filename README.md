# homebridge-http-lock-plus

[![npm](https://img.shields.io/npm/v/homebridge-http-lock-plus.svg)](https://www.npmjs.com/package/homebridge-http-lock-plus) [![npm](https://img.shields.io/npm/dt/homebridge-http-lock-plus.svg)](https://www.npmjs.com/package/homebridge-http-lock-plus)

## Description

This [homebridge](https://github.com/nfarina/homebridge) plugin exposes a web-based locking device to Apple's [HomeKit](http://www.apple.com/ios/home/). Using simple HTTP requests, the plugin allows you to lock/unlock the device.

## Installation

1. Install [homebridge](https://github.com/nfarina/homebridge#installation-details)
2. Install this plugin: `npm install -g homebridge-http-lock-plus`
3. Update your `config.json` file

## Configuration

```json
"accessories": [
     {
       "accessory": "HTTPLock",
       "name": "Lock",
       "openURL": "http://myurl.com/open",
       "closeURL": "http://myurl.com/close"
     }
]
```

### Core
| Key | Description | Default |
| --- | --- | --- |
| `accessory` | Must be `HTTPLock` | N/A |
| `name` | Name to appear in the Home app | N/A |
| `openURL` | URL to trigger unlock | N/A |
| `closeURL` | URL to trigger lock | N/A |

### Optional fields
| Key | Description | Default |
| --- | --- | --- |
| `autoLock` _(optional)_ | Whether your lock should re-lock after being opened | `false` |
| `autoLockDelay` _(optional)_ | Time (in seconds) until your lock will auto lock if enabled | `10` |

### Additional options
| Key | Description | Default |
| --- | --- | --- |
| `timeout` _(optional)_ | Time (in milliseconds) until the accessory will be marked as _Not Responding_ if it is unreachable | `3000` |
| `http_method` _(optional)_ | HTTP method used to communicate with the device | `GET` |
| `username` _(optional)_ | Username if HTTP authentication is enabled | N/A |
| `password` _(optional)_ | Password if HTTP authentication is enabled | N/A |
| `model` _(optional)_ | Appears under the _Model_ field for the accessory | plugin |
| `serial` _(optional)_ | Appears under the _Serial_ field for the accessory | version |
| `manufacturer` _(optional)_ | Appears under the _Manufacturer_ field for the accessory | author |
| `firmware` _(optional)_ | Appears under the _Firmware_ field for the accessory | version |
