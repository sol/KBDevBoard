# KBDevBoard

KBDevBoard is a development board for rapid prototyping of keyboard circuitry.

I use this to test new MCUs with [QMK](https://qmk.fm/) before designing custom
PCBs.

![PCB render](/images/render.png)

## How to use this with `DIRECT_PINS`?

- Connect `DIRECT_PINS` to the pin headers in the middle.
- Connect the five pin headers at the top to `GND`.
- Don't use any of the pin headers at the bottom.
- Soldering the diodes is not required, but it isn't harmful either.

## How to use this with `COL2ROW`?

- Connect `MATRIX_ROW_PINS` to the pin headers at the top.
- Connect `MATRIX_COL_PINS` to the pin headers at the bottom.
- Don't use any of the pin headers in the middle.
- Make sure that you soldered the diodes.

## Why are there ten pin headers for only five rows at the top?

There are two pin headers for each row.  This is convenient when you want to
connect all rows to `GND`.  Use a jumper each to shortcut pin headers `1 + 2`,
`2 + 3`, `3 + 4` and `4 + 5`.  Connect `GND` to one of the two remaning pin
headers `1` or `5`.
