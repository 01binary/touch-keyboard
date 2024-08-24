Hello, I need help with Arduino programming for a monophonic capacitive touch (bass synth) keyboard with 14 keys.

The keyboard will use one AD7147 controller for each key.

Each key is divided into 13 capacitive touch electrodes, corresponding to 13 channels on AD7147.

Arduino should read all channels on all controllers over SPI protocol, detect which keyboard keys are pressed and the position of the finger along the 13 steps that make up the currently pressed key, and send the MIDI messages over Bluetooth.

Output:

1. MIDI messages for keys being pressed and released
2. MIDI control (CC) message for the position of the finger along the currently pressed key.

Research:

I would like the MIDI messages to be transmitted to a Macbook Pro over Bluetooth, so that a sequencer running on the MacBook can receive these messages successfully.

Please select a compact 3.3V compatible Arduino capable of doing this, and if the Bluetooth communication requires another board, then please select the appropriate board.

Hardware:

Once you perform the research to determine which Arduino (and other components like a Bluetooth board) are required for this project, I will create and assemble a PCB with all of these components, and send it to you so that you can debug and test the code.
