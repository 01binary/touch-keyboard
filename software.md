Hello, I need help with Arduino programming for a monophonic capacitive touch (bass synth) keyboard with 14 keys - please quote.

The keyboard will use one AD7147 controller for each key.

Each key is divided into 13 capacitive touch electrodes, corresponding to 13 channels on AD7147.

Arduino Nano 33 BLE should read all channels on all controllers over SPI protocol, detect which keyboard keys are pressed and the position of the finger along the 13 steps that make up the currently pressed key, and send the MIDI messages over Bluetooth.

Only one key can be pressed at the same time, but the finger can be positioned in-between the electrodes within that key, in which case the finger position should be interpolated depending on which electrode it's closest to.

If a second key is pressed while holding the first key, the first key is considered no longer pressed. However, the keys are close together so additional logic may be required to reject false positives (i.e. the keys to either sides of the currently pressed key should not register a press just because the finger is very close to them or only slightly overlaps edges).

The output should be:

1. MIDI messages for keys being pressed and released
2. MIDI control (CC) message for the position of the finger along the currently pressed key. The same CC no matter which key is being pressed. The intention is to control the synth filter sweep by sliding the finger along the pressed key.

Unknowns:

I would like the MIDI messages to be received by a Macbook Pro Bluetooth and work with Ableton Live. If Arduino Nano 33 BLE is not the right controller for this, or additional components are required, then let's adjust the project requirements.

Additional information:

I created a GitHub repository with initial requirements here:
https://github.com/01binary/touch-keyboard

I am working with another person on Fiverr on the PCB design, and now I'm looking for an Arduino programmer for the software part of this project.