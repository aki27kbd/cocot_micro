# Build Guide

![cocot_micro_main00](/images/main_00.jpg)

This page is the build guide for cocot micro.

cocot micro is a DIY trackball composed of mechanical keyboard components. You can use it as a trackball mouse as well as a macro pad with a pointing device.

## Parts
### What's included

|Name|Number|Remarks|
|---|---|---|
|PCB|1||
|Mouse Sensor (PMW3360)|1||
|Ring Encoder (PER601)|1||
|M3 Screw 10mm|3||
|M3 Nut|3|
|M2 Screw 8mm|2|
|M2 Nut|2||
|M2 Screw 3mm|8|
|M2 Spacer 4mm|4||
|Rubber Feet|4||
|3D Printed Ball Base|1||
|3D Printed Ball Cover|1||
|3D Printed Keycaps|8|Optional|
|3D Printed Case|1|Optional|


### What's not included

|Name|Number|Remarks|
|---|---|---|
|MX Switch|8||
|34mm Trackball|1||
|USB-TypeC Cable|1||


## Assembly
### Parts Confirmation

  First, please make sure that you have all the parts listed in the kit accessories.  
  Please start assembling after you have prepared the "other necessary items" as described above.

  - If PCBs come with tabs, break off the tabs and lightly file the cut surfaces.
  - If you are not using a 3D printed case, paint the sides of the PCB black with an permanent marker to make it look better.


### Mouse Sensor

  Place the mouse sensor (PMW3360) on the bottom side of the PCB in the orientation shown in the photo, and solder from the top. Be careful to align the ● mark on the silk with the ● mark on the board.    
  ![cocot_micro_bg_01_1](/images/bg_01_1.jpg)

  Fix the sensor with masking tape so they do not move while soldering. Solder the 16 legs from the top side.  
  ![cocot_micro_bg_01_2](/images/bg_01_2.jpg)

  Remove the kapton tape on the sensor and put lens.
  ![cocot_micro_bg_01_3](/images/bg_01_3.jpg)


### Ball Base Assembly

  Fix the bearing roller with the bearing rollers, M3 screws, and M3 nuts in the orientation shown in the photo. Of the two sides of the three pillars supporting the bearing, it is the side with protrusions that the bearing is fixed to and the flat side that the nut touches.
  ![cocot_micro_bg_02_1](/images/bg_02_1.jpg)

  ![cocot_micro_bg_02_2](/images/bg_02_2.jpg)

  Place the ball base on the PCB with the mouse sensor fixed and the lens attached. Fix with M2 8mm screws from the top side and nuts from the bottom side.
  ![cocot_micro_bg_02_3](/images/bg_02_3.jpg)

  ![cocot_micro_bg_02_4](/images/bg_02_4.jpg)


### Ring Encoder

  Insert the ring encoder from the top of the PCB and solder on the bottom side.  
  ![cocot_micro_bg_03_1](/images/bg_03_1.jpg)

  ![cocot_micro_bg_03_2](/images/bg_03_2.jpg)


### Key Switch

  Insert the 8 key switches from the top of the PCB and solder 2 pins for each switch. Note the orientation of the switches so that they are on the top of the PCB.
  ![cocot_micro_bg_04_1](/images/bg_04_1.jpg)

  ![cocot_micro_bg_04_2](/images/bg_04_2.jpg)


### Assembly

  Fix the tray case (or bottom plate) and PCB using 3mm screws and 4mm spacers.  
  ![cocot_micro_bg_05_1](/images/bg_05_1.jpg)

  ![cocot_micro_bg_05_2](/images/bg_05_2.jpg)

  Attach rubber feet in 4 places on the bottom side.
  ![cocot_micro_bg_05_3](/images/bg_05_3.jpg)

  Attach the ball cover to the ring encoder. If it is loose, tape or otherwise secure it on the inside.
  ![cocot_micro_bg_05_4](/images/bg_05_4.jpg)

  Attach the keycaps. If the 3D printed Keycaps are loose, put plastic wrap or other thin film on the stem of key switch to prevent it from falling out.
  ![cocot_micro_bg_05_5](/images/bg_05_5.jpg)

  Attach the ball and complete.
  ![cocot_micro_bg_05_6](/images/bg_05_6.jpg)


## Firmware

  PCB is delivered with the default firm flashed. If you wish to write your own firm, please follow the instructions below.

  - Press the RESET button while holding down the BOOT button on the bottom to enter boot loader mode.
  - In that state, drag and drop a [.uf2](https://github.com/aki27kbd/cocot_micro/blob/main/firmware/aki27_cocot_micro_auto_mouse.uf2) The farm is written by dragging and dropping the file.

  Keymap is editable from [vial](https://vial.rocks/).  

  ![vial](/images/vial.jpg)


  Source code is available from [here](https://github.com/aki27kbd/vial-qmk/tree/vial/keyboards/aki27/cocot_micro).  


## Custom Keycodes

  Several custom key codes can be set for trackball operation.

  Keycode   |Description
  ---------|-----------
  `CPI_SW`  |Change the CPI of the trackball. With the default firmware, each press changes the CPI in the following order: 200 -> 400 -> 800 -> 1600 -> 3200 -> 200....
  `SCRL_SW` |Changes the sensitivity of the sensor in scroll mode. The higher the value, the smaller the amount of scrolling.
  `ROT_R15` |Turns the Y axis of the mouse sensor 15 degrees clockwise.
  `ROT_L15` |Rotate the Y axis of the mouse sensor 15 degrees counterclockwise.
  `SCRL_MO` |Enables scroll mode for as long as it is pressed.
  `SCRL_TO` |	Toggles between scroll mode and mouse mode each time it is pressed.
  `SCRL_IN` |Inverts the scroll direction.

  Custom key codes can be set in vial using the custom key code under the User tab.  
  ![CustomKeycode_rev](/images/CustomKeycode.jpg)


## Notes
If you have any problems, please contact us at [Twitter account](https://twitter.com/aki27kbd).

Also, it would be very encouraging if you could upload the completed photos to social networking sites. (If you don't feel comfortable uploading your photos, you can send them directly to us via DM.)

The hashtag is #cocot_micro.
