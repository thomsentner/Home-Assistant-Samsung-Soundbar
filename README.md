# SmartThings Soundbar

Adds support for SmartThings-enabled Soundbar

# Features

- Turn on/off
- Set volume
- Step volume up/down
- Mute/unmute
- Select source
- Show current volume level
- Show current state: on/off/playing/paused/idle
- Show if muted/unmuted
- Show current source

# Set up
Make sure your device is logged into your SmartThings account.

Obtain an API key from https://account.smartthings.com/tokens

Go [here](https://graph-eu01-euwest1.api.smartthings.com/device/list) for your device id for each device. Click on the name of your device and the device id will be in the URL

> https://graph-eu01-euwest1.api.smartthings.com/device/show/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXX

In your configuration.yaml add:

```
media_player:
  - platform: smartthings_soundbar
    name: Soundbar
    api_key: "YOUR API KEY"
    device_id: "YOUR DEVICE ID"
```

Tested on:

Samsung HW-Q80R
Samsung HW-Q70R
