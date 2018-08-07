# README #

The original [cinco](https://github.com/sifive/cinco) repo allows to program Freedom E300 boards using the Arduino IDE on **Linux** and **MacOS** only.

This repository allows to program Freedom E300 boards using the Arduino IDE on **Windows** also.

## Notes: ##
1. Tested with Arduino IDE 1.6.12 - 1.8.5 on Windows.
2. Tested with HiFive1 board only.
3. Tested for standard and portable installations.

# Setup on Windows OS #

## Install USB driver

Connect HiFive1 board to computer by USB cable.
Download HiFive1_Driver [https://github.com/MichaelZaidman/CincoWinPkg/releases/download/v1.1/HiFive1_Driver.exe](https://github.com/MichaelZaidman/CincoWinPkg/releases/download/v1.1/HiFive1_Driver.exe)
Install HiFive1_Driver.

## Install Arduino ##

Download and install Arduino IDE tarball from the Arduino website. Unpack it and run their installation script as directed.

## Install the SiFive Boards ##

Add the [https://raw.githubusercontent.com/MichaelZaidman/CincoWinPkg/master/package_sifive_index.json](https://raw.githubusercontent.com/MichaelZaidman/CincoWinPkg/master/package_sifive_index.json)
to the Additional Boards Manager URLs in the `Preferences->Settings`.

Use the Boards Manager to search for and install the "SiFive" boards.

# Setup Your Board #

## Select the board: ##
```
Tools->Board->HiFive1
```
## Select serial COM port: ##
```
Tools->Port
```

## Select OpenOCD as the Programmer ##
```
Tools->Programmer->SiFive OpenOCD
```

# Compile and Upload #

## Basic Example ##

Select the `File->Examples->Basics->Blink` built-in example.

Hit the "Verify" button to test the program compiles,
then "Upload" to program to your board. The green LED should blink.

## RGB LED Examples ##

The RGB Blink example:
`File->Examples->RGB LED->RgbLedBlinkByLib`

The below examples achieve the same fade effect as in the led_fade example supplied with Freedom Studio.
`File->Examples->RGB LED->RgbLedFade`
`File->Examples->RGB LED->RgbLedFadeByLib`
