## Adafruit USB Type C Power Delivery Dummy Breakout - I2C or Fixed - HUSB238 PCB

<a href="http://www.adafruit.com/products/5807"><img src="assets/5807.jpg?raw=true" width="500px"><br/>
Click here to purchase one from the Adafruit shop</a>

PCB files for the Adafruit USB Type C Power Delivery Dummy Breakout - I2C or Fixed - HUSB238. 

Format is EagleCAD schematic and board layout
* https://www.adafruit.com/product/5807

### Description

The HUSB238 USB PD sink chip is neat in that you can either use jumpers (really, resistor selection) to set the desired PD voltage and current or you can use I2C for dynamic querying and setting. We've build a nice Adafruit USB Type C Power Delivery Dummy Breakout board around the HUSB238 to make it very easy to configure and integrate without having to solder any tiny resistors.

It's perfect for use with USB Type C wall adapters that can provide multiple voltages, the standard offerings are 5V, 9V, 12V, 15V, 18V and 20V. This HUSB238 breakout plugs into the USB C cable and then over the CC lines will negotiate the PD request and commands. For example we can ask what voltages are available and then pick the highest one. Or if you need a specific voltage it will specifically select that one.

This breakout will be handy for projects where you need a lot more than 5V @ 2A power: this adapter can give up to 20V at 5A - yes you can get 100W over USB C! - and you could buck that down to get a ton of current at 5V or 12V if that's needed. Or use it to convert a DC or battery-powered device into a USB C powered one!

Jumper-configured usage is simple: by default its hard-wired for 5V 1A output since that's what USB C will always provide at first. Cut the 5V jumper and solder closed the 9V, 12V, 15V, 18V or 20V jumper to select the resistor that sets the voltage. You can also select the desired current from 2A to 3A, although we have found that this isn't as essential, you could always just pull as much as the adapter will provide. No microcontroller or microcomputer is required!

I2C-configured usage is a little more challenging. Since the Vout can be as high as 20V we don't have an onboard voltage regulator or pullup resistors. Connect to a microcontroller or microcomputer board that has a separate power supply (or that can regulate from up-to-20V if you plan on selecting that high) and I2C pullup resistors to your desired logic level. Then use the Arduino library and example code to query the USB Type C PD source for available voltages and currents and select the desired voltage dynamically. When configuring over I2C, the jumper settings are used on startup until the I2C commands come over.

Comes with a small bit of header and a terminal block so you can decide whether you want to use it in a breadboard, or free-wired.

### License

Adafruit invests time and resources providing this open source design, please support Adafruit and open-source hardware by purchasing products from [Adafruit](https://www.adafruit.com)!

Designed by Limor Fried/Ladyada for Adafruit Industries.

Creative Commons Attribution/Share-Alike, all text above must be included in any redistribution. 
See license.txt for additional details.
