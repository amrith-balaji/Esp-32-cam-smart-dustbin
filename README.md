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
3D Print the four stl files given 
## Assembly :
1) the servo is placed between the rods pertruding outwards in the file - Dustbin_camera-stand.stl , with the stand for the camera on top
2) The servo is placed on the cutout given in the file - Dustbin_body.stl
3) Place for the servo horn is left in the file - Dustbin_lid.stl
4) A small hole is give in both the files - Dustbin_lid & Dustbin_body.stl for a rod to act as support
5) Dustbin_cover is placed above the body of the dustbin to help avoid errors in object identification

The final assembly looks like this :
![IMG_7555](https://github.com/amrith-balaji/Esp-32-cam-smart-dustbin/assets/124582454/16c6623b-a3a0-45db-abc2-5c89150ef906)
![IMG_7554](https://github.com/amrith-balaji/Esp-32-cam-smart-dustbin/assets/124582454/0645c677-f799-4998-b3d8-8f8a20f3097f)

# Part - III data aquisition and training 
## Data Aquisition :
1) Download the Esp32 cam eloquent library from the library manager in arduino or the github : ``` https://github.com/eloquentarduino/EloquentEsp32cam ```
2) execute the program 26_Collect_Images found in : File > Examples > ELoquentEsp32cam > 26_Collect_Images
3) enter your SSID & Password and upload the code
4)  you should get the following serial monitor output : ![image](https://github.com/amrith-balaji/Esp-32-cam-smart-dustbin/assets/124582454/7fc60c0b-c0b6-4349-ac52-cf39c075a1dd)
5)  Type the ip address in your browser and you should end up in the following webpage : ![image](https://github.com/amrith-balaji/Esp-32-cam-smart-dustbin/assets/124582454/e06f542e-66cf-4cc9-bc44-d29c1db4ab3a)
6)  Collect the images and enter the label for them . The label should be corresponding to the image as it is important for the later steps. (eg. image of a banana , label: banana)

## Training the model
1) login to edge impulse : ``` https://edgeimpulse.com ``` and click on new project
2) click on add data. Select upload mode as select a folder and upload your files
3) 

