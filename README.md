# bluetooth-keyboard and mouse

This PXT package allows the micro:bit to act as a Keyboard or mouse peripheral.

## Usage Keyboard

Place a ``||bluetooth start keyboard service||`` block in your program to enable Bluetooth LE Keyboard.
With this block, the `micro:bit` starts advertise BLE packets as a Keyboard peripheral.

```blocks
bluetooth.startKeyboardService();
```

**TBD**
To Send `Hello World!` to the paired host, place block like this:

```blocks
bluetooth.keyboardSendText("Hello World!");
```

##
 Usage Mouse
Place a ``||bluetooth start mouse service||`` block in your program to enable Bluetooth LE Mouse.
With this block, the `micro:bit` starts advertise BLE packets as a Mouse peripheral.

```blocks
bluetooth.startMouseService();
```

For example, hold left mouse button :

```blocks
bluetooth.setMouseButton(MouseButton.MOUSE_BUTTON_LEFT, ButtonState.BUTTON_DOWN);
```

For example, move mouse pointer using acceleration of micro:bit :

```blocks
basic.forever(() => {
    bluetooth.setMouseSpeed(input.acceleration(Dimension.X) / 8, input.acceleration(Dimension.Y) / 8, 0);
}
```


## Supported Platforms

Currently, tested with `micro:bit` and `Android` host only.
Mac OS X can connect with `micro:bit`, but it can't receive Keyboard message.

## Supported targets

* for PXT/microbit

(The metadata above is needed for package search.)

## License

MIT

```package
bluetooth
bluetooth-keyboard=github:kshoji/pxt-bluetooth-keyboard
```
