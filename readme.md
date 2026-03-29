# ZMK Corne Keyboard Layout

This this my personal [zmk](https://github.com/zmkfirmware/zmk) config for my
[corne keyboard](https://github.com/foostan/crkbd), the firmware is built to
work with the following devices.

- Keyboard: Corne 6 column
- Controller: nice!nano v2 (for both left and right keyboard)

> Standard split setup: left half is central, right half is peripheral.

## The Keyboard

![typeractive_kb](https://github.com/DarrenVictoriano/zmk-config/blob/master/images/kb.jpeg)

## Keymaps

These are the keymaps and layers defined in this config. The keymaps were
generated using
[Nick Coutsos's Keymap Editor](https://nickcoutsos.github.io/keymap-editor/).

![keymaps](https://github.com/DarrenVictoriano/zmk-config/blob/master/images/corne.svg)

## Macros

- ⚡️ : hyper key (`ctrl` + `shift` + `alt` + `cmd`)
- ⚙️ : system settings (`cmd` + `shift` + `J`)
- 📷 : `printscreen` (linux) / `F13` (macos)
- `⌘⌥⎵` : homerow
- `⌃⎵` : tmux leader key
- `✦⎋`: `ctrl` + `shift` + `esc`
- adjust layer circle arrows: mouse movements
- adjust layer pan-arrows: scroll movements

> The image is generated using
> [Cem Aksoylar's Keymap-drawer](https://github.com/caksoylar/keymap-drawer)

## Handwired Matrix Pins

These are the matrix GPIO mappings used by the custom shield overlays.

### Left (central)

- row-gpios: `P1.00`, `P0.11`, `P1.04`, `P1.06`
- col-gpios: `P0.09`, `P1.11`, `P0.10`, `P0.02`, `P1.15`, `P1.13`

### Right (peripheral)

- row-gpios: `P0.02`, `P1.11`, `P0.10`, `P0.09`
- col-gpios: `P1.06`, `P0.11`, `P1.04`, `P0.22`, `P0.24`, `P1.00`

## Installing Firmware

Whether you built it yourself or downloaded my prebuilt firmware, it should
contain the following files:

For Keyboard (Corne):

- nano_corne_left.uf2
- nano_corne_right.uf2
- nano_reset_settings.uf2

> The `*_reset_settings.uf2` file is used to clear persistent settings like
> default layers, BLE pairings, and other saved data that may remain after
> repeatedly flashing new firmware.

### Steps

1. Plug in your left Corne keyboard (central side).
2. Double-press the side button to enter bootloader mode.
3. Copy `nano_reset_settings.uf2` to the keyboard's root folder. (Optional, but
   recommended to ensure a clean slate.)
4. After the error appears, unplug and replug the keyboard.
5. Double-press the button again to re-enter bootloader mode.
6. Copy `nano_corne_left.uf2` to the device.
7. Unplug after flashing, then repeat steps 1–6 for your right Corne using
   `nano_corne_right.uf2`.
8. Turn on both sides. Enjoy!
