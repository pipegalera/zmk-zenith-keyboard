# Zenith Keyboard

  <table>
    <tr>
      <td><img src="images/zenith_keyboard.png" alt="Zenith Keyboard"></td>
      <td>
        <p>Zenith is cool 6 columns version of the the TOTEM split keyboard, designed by the people at <a href="https://ergomech.store/">ergo mech shop.</a></p>
        <p>The controllers are the Seeeduino XIAO BLE (<code>nRF52840</code>). I had no trouble pairing the halves with MacOS M series, Windows 11, and Arch Linux.</p>
      </td>
    </tr>
  </table>

## Keymap Diagram

![Zenith Keymap](keymap-drawer/zenith.svg)

## Keyboard layout

| Layer    | Activation   | Description                                                  |
| -------- | ------------ | ------------------------------------------------------------ |
| **BASE** | Default      | QWERTY layout with modifiers                                 |
| **SYM**  | Hold `F`     | Symbols                                                      |
| **NUM**  | Hold `Enter` | Numbers and navigation                                       |
| **XTR**  | Hold `ESC`   | Extra layer with function keys, media and bluetooth controls |

[Why this activation setup?](https://gist.github.com/pipegalera/96ebbe37e71e2c9030cf3b9d0725b4fb)

## Connecting the keyboard

1. Trigger the `.github/workflows/build.yml` workflow automatically by pushing a change to the `main` branch.

2. Wait for the workflow to complete and download the firmware artifacts (3 `uf2` files zipped).

3. For both halves. Connect to PC and click twice the reset button on the keyboard. Drag and drop first `settings_reset-seeeduino_xiao_ble-zmk.uf2` before the `zenith_*-seeeduino_xiao_ble-zmk.uf2` file.

4. There is no "on" or "off" led. Make sure the power toggle swith is pointing to the inside of the keyboard (on) - otherwise the keyboard will not be recognized by the PC.
