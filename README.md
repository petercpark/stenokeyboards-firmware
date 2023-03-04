# stenokeyboards-firmware

So you bought a steno keyboard from [StenoKeyboards](https://stenokeyboards.com/)?

This is a place for the default firmware that comes with your steno keyboard, or firmware for your diy kit.

If you want to build from the source code, go to the official [qmk_firmware](https://github.com/qmk/qmk_firmware/tree/master/keyboards/the_uni) repository.

Don't move forward if your keyboard already works and you don't know what you're doing!

## Keyboard and corresponding firmware

| Keyboard      | Folder                      | Firmware Available            | MCU        |
| ------------- | --------------------------- | ----------------------------- | ---------- |
| Uni v1 and v2 | [the_uni_v2](the_uni_v2/)   | Default, Qwerty               | atmega32u4 |
| Uni v3        | [the_uni_v3](the_uni_v3/)   | Default, Qwerty, Utility      | atmega32u4 |
| Uni v4        | [the_uni_v4](the_uni_v4/)   | Default, Qwerty, Utility      | rp2040     |
| Polyglot v1   | [polyglot_v1](polyglot_v1/) | Default, Everything, Switched | rp2040     |

## How to flash Uni v4 (or any rp2040 MCU keyboard)

1. Download your firmware

   - Clone the repo by clicking "Code" -> "Download ZIP".
   - Or `git clone https://github.com/petercpark/stenokeyboards-firmware.git`

2. Unplug the keyboard
3. On the back of the keyboard, press and hold the 'B' (boot) button and while you plug the keyboard in.
4. This will make the computer recognize the keyboard as a storage device and in your file explorer, you will be able to see it.
5. Copy paste the .uf2 file into the keyboard. Paste it into the root folder.\*
6. That's it, very easy.

\*If you are on a Ventura Macbook, you might get an error when pasting it in. In that case see the instructions [here](https://www.raspberrypi.com/news/the-ventura-problem/).

## How to flash v3, v2, and v1 only

1. Download your firmware

   - Clone the repo by clicking "Code" -> "Download ZIP".
   - Or `git clone https://github.com/petercpark/stenokeyboards-firmware.git`

2. Download [QMK Toolbox](https://github.com/qmk/qmk_toolbox/releases/latest) and open it up. It should prompt you to download dependencies when you first open it up. It won't work unless you download the dependencies.
3. Select the .hex file you want to use by clicking "open". Make sure that the MCU matches what is shown on the chart above (i.e. atmega32u4)

   - If you are flashing your keyboard because it didn't work with Plover, try flashing it with the Qwerty .hex file as a test to make sure that the board itself is in working condition.
   - The purpose of doing this is to make sure that the keyboard is working properly without having to worry about configuring around with Plover.

4. Click "auto flash" and hit the reset button wherever that may be (probably on the back somewhere), or you can short GND and RST on the pro micro.
5. Open Plover and connect machine to see it work. See the [docs](https://docs.stenokeyboards.com/) for information on setting up your steno keyboard with Plover.
   - If you flashed the Qwerty firmware: make sure that the keyboard outputs letters like a normal keyboard would. If it works, you can change Plover's machine settings to "keyboard" instead of GeminiPR and you can just steno like that. However, this is not recommended.
   - It is recommended that you flash it again with the default GeminiPR firmware and go through configuration again. With GeminiPR, you can use steno and use a normal keyboard at the same time.
