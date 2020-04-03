# SmartThings Soundbar


[![hacs_badge](https://img.shields.io/badge/HACS-Custom-orange.svg)](https://github.com/custom-components/hacs)
[![buymeacoffee_badge](https://img.shields.io/badge/Donate-buymeacoffe-ff813f?style=flat)](https://www.buymeacoffee.com/PiotrMachowski)


Adds support for SmartThings enabled Soundbar

## Features

- Turn on/off 
- Set volume
- Step volume up/down
- Mute/unmute
- Select source
- Show current volume level
- Show current state: on/off/playing/paused/idle
- Show if muted/unmuted
- Show current source


## Configuration options

| Key | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `name` | `string` | `False` | `SmartThings Soundbar` | Name of soundbar |
| `api_key` | `string` | `True` | - | SmartThings API key (see: [here](#Getting API key and device id)) |
| `device_id` | `string` | `True` | - | SmartThings device id (see: [here](#Getting API key and device id)) |
| `max_volume` | `positive integer` | `False` | 100 | Volume level that will be used as a maximum level in Home Assistant |

## Example usage

```yaml
media_player:
  - platform: smartthings_soundbar
    name: Soundbar
    api_key: "YOUR API KEY"
    device_id: "YOUR DEVICE ID"
    max_volume: 30
```


## Getting API key and device id

Make sure your device is connected to yout SmartThings account.

Obtain an API key from https://account.smartthings.com/tokens

Go [here](https://graph-eu01-euwest1.api.smartthings.com/device/list) for your device id for each device. Click on the name of your device and the device id will be in the URL

> https://graph-eu01-euwest1.api.smartthings.com/device/show/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXX


## Installation

Download [*media_player.py*](https://github.com/PiotrMachowski/Home-Assistant-custom-components-SmartThings-Soundbar/raw/master/custom_components/smartthings_soundbar/media_player.py)
and [*manifest.json*](https://github.com/PiotrMachowski/Home-Assistant-custom-components-SmartThings-Soundbar/raw/master/custom_components/smartthings_soundbar/manifest.json) to `config/custom_components/smartthings_soundbar` directory:
```bash
mkdir -p custom_components/smartthings_soundbar
cd custom_components/smartthings_soundbar
wget https://github.com/PiotrMachowski/Home-Assistant-custom-components-SmartThings-Soundbar/raw/master/custom_components/smartthings_soundbar/media_player.py
wget https://github.com/PiotrMachowski/Home-Assistant-custom-components-SmartThings-Soundbar/raw/master/custom_components/smartthings_soundbar/manifest.json
```



Tested on:

- Samsung HW-Q80R
- Samsung HW-Q70R


<a href="https://www.buymeacoffee.com/PiotrMachowski" target="_blank"><img src="https://bmc-cdn.nyc3.digitaloceanspaces.com/BMC-button-images/custom_images/orange_img.png" alt="Buy Me A Coffee" style="height: auto !important;width: auto !important;" ></a>
