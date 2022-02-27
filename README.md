# stenokeyboards-firmware

So you bought a steno keyboard from [StenoKeyboards](https://stenokeyboards.com/)?

This is a place for the default firmware that comes with your steno keyboard, or firmware for your diy kit.

Don't move forward if you don't know what you're doing!

## Keyboard and corresponding firmware

| Keyboard      | Mode    | Firmware                                                                                                                         | MCU        |
| ------------- | ------- | -------------------------------------------------------------------------------------------------------------------------------- | ---------- |
| Uni v1 and v2 | Default | [the_uni_pro_micro_default.hex](https://github.com/petercpark/stenokeyboards-firmware/blob/master/the_uni_pro_micro_default.hex) | atmega32u4 |
| Uni v3        | Default | [the_uni_usb_c_default.hex](https://github.com/petercpark/stenokeyboards-firmware/blob/master/the_uni_usb_c_default.hex)         | atmega32u4 |
| Uni v3        | Qwerty  | [the_uni_usb_c_qwerty.hex](https://github.com/petercpark/stenokeyboards-firmware/blob/master/the_uni_usb_c_qwerty.hex)           | atmega32u4 |

## How to flash

1. Download your firmware

- right clicking on the file and click "save link as".
- Or clone the repo by clicking "Code" -> "Download ZIP".
- Or `git clone https://github.com/petercpark/stenokeyboards-firmware.git`

2. Download [QMK Toolbox](https://github.com/qmk/qmk_toolbox/releases/latest) and open it up. Download dependencies if it asks you to.
3. Select the .hex file you downloaded by clicking "open". Make sure that the MCU matches what is shown on the chart above (i.e. atmega32u4)
4. Click "auto flash" and hit the reset button wherever that may be (probably on the back somewhere), or you can short GND and RST on the pro micro.
5. Open Plover and connect machine to see it work. See the [docs](https://docs.stenokeyboards.com/) for information on setting up your steno keyboard with Plover.
