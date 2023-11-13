## Parts Requied : 

Esp-32 cam    - 1x (Brains) 

Servo (9g)    - 1x (Motor)

Jmper wires   - 10x (Wires?)

FTDI adapter  - 1x (Accessing the Brains)

3d printed parts - 1x (each) (structure??)



# Part - I Getting the Esp-32 cam set up
## Connecting the Esp 32 cam to the FTDI module :
![image](https://github.com/amrith-balaji/Esp-32-cam-smart-dustbin/assets/124582454/3a00c1c8-cc09-4c16-a06a-16e12c017145)

Connections :
Esp-32 cam  | FTDI module 
------------- | -------------
GND | GND
5V  | 5V
UOR | TX
UOT | RX

``` Important: GPIO 0 of the ESP-32 cam needs to be connected to GND so that you’re able to upload code. ```

## Uploading to the board :
to upload code to the ESP32-CAM using Arduino IDE, follow the next steps:

1) Go to Tools > Board and select AI-Thinker ESP32-CAM. You must have the ESP32 add-on installed. Otherwise, this board won’t show up on the Boards menu.
2) Go to Tools > Port and select the COM port the ESP32-CAM is connected to.
3) For demonstration purposes, you can upload a blank sketch to your board
4) When you start to see some dots on the debugging window, press the ESP32-CAM on-board RST button.
5) for any errors in these steps , refer to online sources for help
   
# Part - II The frame
