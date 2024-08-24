# touch-keyboard

Capacitive Touch Keyboard Requirements

- Capacitive touch electrodes
- AD7147 controllers
- Arduino Nano 33BLE
- Adafruit Lipo Backpack

The keyboard should have 14 keys, each divided into 13 capacitive touch electrodes.
I would like to use the AD7147 controller from Analog Devices, which supports 13 capacitive touch inputs. The PCB will need 14 of these AD7147 chips, one for each keyboard key.

I am attaching an initial proposed electrode layout in SVG format with 1mm spacing between keys, and 0.5mm spacing between electrodes within each key. This makes each electrode 9mm x 10mm. If the spacing needs to be adjusted, we can't modify the positioning of the electrode centers, only shrink the electrodes to a smaller size - once you tell me the required spacing I can adjust electrode sizes and re-submit the layout.

All of the AD7147 controllers need to be routed to a pin header designed to communicate with Arduino Nano 33 BLE over SPI protocol.

Finally, Arduino Nano 33 BLE will need to get its power from Lipo Backpack (https://www.adafruit.com/product/2124). If Arduino Nano 33 BLE layout is on the PCB, place the Backpack component next to it, and route the 3.3V power to Arduino Nano and to each of the AD7147 controllers.
