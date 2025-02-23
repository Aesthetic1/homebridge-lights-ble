# homebridge-lights-ble

This plugin let you control BLE lights.

Control On/Off, Hue, Saturation and Brightness.

## Prerequisite
You need to have a bluetooth device. Check using `hcitool dev` command. You may also need root access with Homebridge

To run without root access, go to homebridge terminal and type ```sudo setcap cap_net_raw+eip $(eval readlink -f `which node`)```

## Installation

`npm i homebridge-lights-ble`

## Configuration
```js
{
    "accessory": "LedStrip", // Dont change
    "name": "LED", // Accessory name
    "uuid": "be320202f8e8" // BLE device UUID
}
```

To find your device uuid, use `hcitool lescan`, grab the device uuid, remove all ':' and use lowercase alpha characters

## Contribution
You can contribute by creating merge request, you can find a documentation of the BLE message used here : [Documentation](https://github.com/arduino12/ble_rgb_led_strip_controller/blob/master/README.md)
