# Eryone ER-20 3D Printer Firmware
###  (Based on Marlin 2.0.8)

![GitHub Stars](https://img.shields.io/github/stars/Eryone/STM32.svg)
![GitHub contributors](https://img.shields.io/github/contributors/Eryone/STM32.svg)
![GitHub followers](https://img.shields.io/github/followers/Eryone.svg)

### Warning
- **When you uploaded the firmware. You need calibrate the Z again. Flash firmware will reset the EEPROM!!
- **Before of all, if you are not familiar with the Marlin firmware editing. Please don't modify it and we suggest you use the prepared firmware. The modify incorrectly has the risk of damage your printer.**
- **If your slicer don't have this gcode. You need to add the G29 to your start gcode. The Cura4.9 or higher support the ER20, it prepared this so you don't need to add it. But you may need to add G29 for the Prusa slicer, simplfiy3d,etc.**


## Code contributor: 
  - **Stefano Piga**
  - **Matt W.**
  - **Peter Chung**
  - **Adriano De Cillis**
  - **Eryone** 

## Source               

- *[Marlin officail](https://github.com/MarlinFirmware/Marlin)* Marlin offical firmware release main page
- *[Marlin Gcode](https://marlinfw.org/meta/gcode/)* Marlin offical gcode introduction

## Feature
#### Main feature
- S_Curve Acceleration
- LIN_Advanced K
- Prepared the en version and multi-language version
- **If you flash the multi-language version and printer blue screen.**
- **Please flash the en version then it will works**
- Powerloss recovery
(Default off, if you need to use then go to LCD menu enable it)


#### Support Filament runout sensor/E3D Hotend/Direct drive extruder
- **How to use it? Go to configuration.h, delete"//" to enable which one you want to use**
###### //#define ER20_FL         // Enalbe for ER20 Filament runout sensor
###### //#define ER20_E3D        // Enalbe for ER20 E3D extruder
###### //#define ER20_Direct     // Enable for ER20 Direct drive extruder

#### About More
- Motherboard cooling fan*Half speed/40C
- Bed leveling 25points/36points detect
- Calibrate Gantry
- Auto bed leveling homing speed cofnig switch
- PID auto tune menu
- SD card print percentage
- **Calibrate Z menu moved to "Configuration">"Advanced setting">"Calibration offsets"**
- For the auto bed leveling, if you want to set thte abl to 9 points instead of 25 points.
Refer to this post then compline it: https://www.eryone.com/forum/viewtopic.php?f=9&t=468


## Compared with ER20 Firmware 2.0.5.3
- Fixed eeprom reset error
- Fixed Auto-PID frezzing error
#### Extend info:
- For Auto-PID, we suggest the user do it more than 6 times.Then find out the average value then set it
- If you find the temperature raise too fast, try to decrease the PID-I value
- If you find the tempreature raise too slow, try to increase the PID-I value
- **Update the marlin version to 2.0.8**


## Build and Install
#### 1. To flash, connect up your printer to your PC via the USB lead. Make sure the PSU of the printer is on.

#### 2. Go to "Flashtool">"Windows", "MAC OS", "Linux X86_64" or "Linux arm" folder.

#### 3. Flash toolkit at different system
#### 1) For windows users:
- Start the "FlashTool_STM32.exe", make sure you are on the right com port to double-check just unplug your printer and click refresh, the right one will be displayed at the window. 
- Select the "factory firmware.bin" and it will ask you to reset your printer, do this by pressing the little button under the knob on the LCD screen
**(The button is short and hard to click because it can prevent accidental click. You can use the Allen key to click it)**

#### 2) For mac os users:
- Extract the zip file.
- Then Double Click the .app file to run it.
- Select the appropriate Serial Port. (Use Refresh ports button to refresh Serial Port list)
- Click on Download Button and select the proper BIN file.
- If problem occurs in step 2 then kindly copy and paste the full path of the .bin file in the text box and then Click on the Download Button.
- Wait for the process.

#### 3) For linux users:
#### IMPORTANT INFO:
On Windows and macOS systems the users are allowed to communicate over serial ports. 
But on Linux systems the users are not allowed to communicate over serial ports by default (this is for security reasons in Linux). So to allow the current user to communicate over Serial Ports, we need to follow these steps just one time. After following these steps the user can then communicate over serial ports. After following these steps one time, the user does not need to do anything else to access the serial ports.

- Open Terminal and type:
sudo usermod -a -G dialout $USER

- Log out and Log in again. 

- If the problem still remains after step 1 and 2, then restart computer.



#### INSTRUCTIONS TO RUN THE APP:

- Right click the .AppImage file and click on Properties.
- Click on Permissions.
- The checkbox "Allow executing file as program" should be checked/ticked.
(This is standard procedure for running Linux AppImage Apps)

- Then Double Click the App file to run it.


#### INSTRUCTIONS WHEN APP IS RUNNING:
- Select the appropriate Serial Port. (Use Refresh ports button to refresh Serial Port list)
- Click on Download Button and select the proper BIN file.
- If problem occurs in step 2 then kindly copy and paste the full path of the .bin file in the text box and then Click on the Download Button.
- Wait for the process.

#### 4. Let it flash and reboot and away you go

## Join our group& Contact us
- *[Facebook](https://www.facebook.com/groups/247271792709370/)*
- *[Instagram](https://www.instagram.com/eryone3d/)*
- *[Eryone Forum](https://www.instagram.com/eryone3d/)*
- *[Youtube](https://www.youtube.com/eryone3d)*




 




 
