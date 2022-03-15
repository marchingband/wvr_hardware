# wvr_hardware

Find the Kicad files in their respective folders, more will be added with time.  
We have done our best to make these files portable, using project specific libraries.  
These are for Kicad V5.

In the JLC_PCB folder you can find all the files needed to order WVR BASIC from JLC with assembly. Kindly donated by Robin of Atonal Circuits.
  
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
D6      |       8          |    0       | no ADC when WIFI active  
D7      |       7          |    36      | no built-in pullups  
D8      |       6          |    39      | no built-in pullups  
D9      |       5          |    34      | no built-in pullups  
D10     |       4          |    35      | no built-in pullups  
D11     |       3          |    32      |  
D12     |       2          |    33      |  
D13     |       1          |    27      | no ADC when WIFI active  
</pre>
