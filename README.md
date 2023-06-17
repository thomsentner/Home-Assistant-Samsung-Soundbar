[![GitHub Latest Release][releases_shield]][latest_release]
[![GitHub All Releases][downloads_total_shield]][releases]
[![PayPal.Me][paypal_me_shield]][paypal_me]

# SmartThings Soundbar

Adds support for SmartThings enabled Soundbar

## Features

- Turn on/off
- Set volume
- Step volume up/down
- Mute/unmute
- Select source
- Select soundmode
- Show current volume level
- Show current state: on/off/playing/paused/idle
- Show if muted/unmuted
- Show current source

## Configuration options

| Key          | Type               | Required | Default                | Description                                                                                                                                               |
| -------------- | -------------------- | ---------- | ------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `name`       | `string`           | `False`  | `SmartThings Soundbar` | Name of soundbar                                                                                                                                          |
| `api_key`    | `string`           | `True`   | -                      | SmartThings API key (see:[here](https://github.com/PiotrMachowski/Home-Assistant-custom-components-SmartThings-Soundbar#getting-api-key-and-device-id))   |
| `device_id`  | `string`           | `True`   | -                      | SmartThings device id (see:[here](https://github.com/PiotrMachowski/Home-Assistant-custom-components-SmartThings-Soundbar#getting-api-key-and-device-id)) |
| `max_volume` | `positive integer` | `False`  | 100                    | Volume level that will be used as a maximum level in Home Assistant                                                                                       |

## Examples usage

```yaml
smartthings_soundbar:
  devices:
    - name: Barre de son
      api_key: b13391c7-8cef-4518-a58e-393b079b4bf5
      device_id: da93855b-45cd-6ca0-86d6-2c9570165eb8
      max_volume: 100
```

## Device

this integration creates a device
composed of a media player and 3 switches
- bass_boost
- Night_mode
- voice_amplifier

You can group them on an entities card

![Alt text](entities_card.png)

## Getting API key and device id

Make sure your device is connected to yout SmartThings account.

Obtain an API key from https://account.smartthings.com/tokens

Go [here](https://graph-eu01-euwest1.api.smartthings.com/device/list) for your device id for each device. Click on the name of your device and the device id will be in the URL

> https://graph-eu01-euwest1.api.smartthings.com/device/show/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXX

## Installation

### Manual

To install this integration manually you have to download [*smartthings_soundbar.zip*](https://github.com/ThierryBourbon/Home-Assistant-custom-components-SmartThings-Soundbar/blob/master/smartthings_soundbar.zip) and extract its contents to `config/custom_components/smartthings_soundbar` directory:

```bash
mkdir -p custom_components/smartthings_soundbar
cd custom_components/smartthings_soundbar
wget https://github.com/ThierryBourbon/Home-Assistant-custom-components-SmartThings-Soundbar/blob/master/smartthings_soundbar.zip
unzip smartthings_soundbar.zip
rm smartthings_soundbar.zip
```

### Known problems

* If you have config validation issues after installing this component you have to follow these steps:
  * Install custom component
  * Restart Home Assistant
  * Add configuration
  * Restart Home Assistant again

## Supported devices

This integration was confirmed to work with following devices:

- Samsung HW-N950
- Samsung HW-Q800T
- Samsung HW-Q950T
- Samsung HW-Q990B
- Samsung HW-Q90R
- Samsung HW-Q80R
- Samsung HW-Q70R
- Samsung HW-S60T
- Samsung HW-S61T
- Samsung HW-Q930B

[latest_release]: https://github.com/ThierryBourbon/Home-Assistant-custom-components-SmartThings-Soundbar/releases/tag/latest_release
[releases_shield]: https://img.shields.io/github/release/ThierryBourbon/Home-Assistant-custom-components-SmartThings-Soundbar.svg?style=popout
[releases]: https://github.com/ThierryBourbon/Home-Assistant-custom-components-SmartThings-Soundbar/releases
[downloads_total_shield]: https://img.shields.io/github/downloads/ThierryBourbon/Home-Assistant-custom-components-SmartThings-Soundbar/total
[buy_me_a_coffee_shield]: https://img.shields.io/static/v1.svg?label=%20&message=Buy%20me%20a%20coffee&color=6f4e37&logo=buy%20me%20a%20coffee&logoColor=white
[paypal_me_shield]: https://img.shields.io/static/v1.svg?label=%20&message=PayPal.Me&logo=paypal
[paypal_me]: https://paypal.me/thierryBourbon

