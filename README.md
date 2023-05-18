# wvr_hardware

Find the Kicad files in their respective folders, more will be added with time.  
We have done our best to make these files portable, using project specific libraries.  
These are for Kicad V5.

In the JLC_PCB folder you can find all the files needed to order WVR BASIC from JLC with assembly. Kindly donated by Robin of Atonal Circuits.

There are 3 branches. v2.1 is the newest one, which includes a footprint for the XIAO SAMD21 on the back side, and a resistor on the front side to connect the UARTS.
click "main" above, and select v2.1 to move to this new branch
  
# pinouts

<pre>
pinout for WVR :

WVR PIN | MAKERS BOARD PIN | ESP32 GPIO | NOTES  
  
D0      |       14         |    3       | FTDI RX  
D1      |       13         |    1       | FTDI TX  
D2      |       12         |    21      | USB MIDI In (when using USB backpack firmware)  
D3      |       11         |    19      |  
D4      |       10         |    18      |  
D5      |       9          |    5       |  
D6      |       8          |    0       | no ADC when WIFI active, strapping pin for bootloader mode (must be high or floating at boot)  
D7      |       7          |    36      | no built-in pullups, input only  
D8      |       6          |    39      | no built-in pullups, input only  
D9      |       5          |    34      | no built-in pullups, input only  
D10     |       4          |    35      | no built-in pullups, input only  
D11     |       3          |    32      |  
D12     |       2          |    33      |  
D13     |       1          |    27      | no ADC when WIFI active  
</pre>  
  
# wiring diagram
Example of powering with the 5v pin, instead of the USB jack, with breadboard-compatible push button and headphone jack attached.  
When WVR's WiFi is active, current consumption can peak significantly, as the radio consumes a fair bit of current. We recommend a PSU that provides 500mA or more at 5v. Any voltage between 5vDC and 9vDC will work, but keep in mind that higher voltage will result in more heat produced by the voltage regulator, which can get very hot! If you experience brown-outs during the boot sequence, try a PSU with a higher current rating.  

![wvr wiring diagram](https://github.com/marchingband/wvr_hardware/blob/main/images/wiring-diagram.png)

# wiring diagram for midi control
Example of controlling WVR from a RPi Pico using MIDI. Note that because MIDI is optically isolated, both boards can be powered independantly, by USB, or otherwise. Thus there are no power rails connected in this diagram. It is also OK to power both boards from the same power source, it is just not necissary to do so.  
Note also, the MIDI signal does not use a ground connection. MIDI is a 2-line protocol, just +5v and TX are needed.  
Here is a great Arduino library to generate MIDI signals from the RPi Pico: https://github.com/FortySevenEffects/arduino_midi_library

![wvr wiring diagram](https://github.com/marchingband/wvr_hardware/blob/main/images/wiring-diagram-midi.png)
