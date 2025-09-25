To begin, this repository serves as an archive of my work relating to this project for the purposes of my university studies. All items in this repository are work in progress and are NOT finalized

Having used a set of Cheesecake Blueberry trackers for some time, I quite like them.  The hardware is well designed and the compact design of all the components makes everything extremely comfortable for long-term wear.

However, the ESP-12F processor is the one pain point that I have had with these trackers.  Of the set of 6 modules I purchased and installed on a set of 6 boards, half of them had connectivity issues.  Also, they are quite expensive to get from Digikey at almost 7 USD per piece.  As the ESP8266 has been discontinued by Espressif, there is a limit for how long the ESP12F will be available.  I began this project with two goals; design a new board based on the ESP32-C3, utilize parts only from Digikey to limit the impact of tarrifs, and keep the form factor the same so the boards can be swapped into existing cases.

After a couple weeks of work, this was the result:

![Error](https://github.com/LorcaSnep/SlimeVR-CheeseCake-Neo/blob/main/Images/Cheesecake%20Neo%20Blueberry%20Front.PNG)

![Error](https://github.com/LorcaSnep/SlimeVR-CheeseCake-Neo/blob/main/Images/Cheesecake%20Neo%20Blueberry%20Back.PNG)

For the most part, a lot of the hardware design is complete.  There are a couple edits that I would like to make to the schematic and the silkscreens are not finalized.

I have based this design around the ESP32-C3-WROOM-02-N4 processor.  This is paired with a CP2102 to handle USB communication, and an LSM6DSVTR IMU (hence the design having the "Blueberry" name.




       
## Extra Info:      
Any kind of modification are welcome!         
It can be even better if you can credit me on the modified PCB with [\[This LOGO\]](999-PictureFiles/SK-LOGO.png)     


## Index
- [Components](#Components)
- [Versions](#Versions)
- [Printing](#Printing)
- [Assembly](#Assembly)
- [Support Link](#Support)

## Components 
For the CheeseCake you will need the following components:   
- PCB produced by JLC PCBA   
- 3D Print Parts   
- 38 or 40mm straps   
-   Li-po Battery (_803035 800/900mAh or 903035 1000/1200mAh is what the docs suggest_)
    -   **Ensure the battery is no larger than 9mm in depth, 30mm in width, and 35mm in height to fit the case.**
    -   **Verify the battery dimensions with the seller before purchase. Some sellers list 803035 batteries with dimensions exceed, which will not fit in the 3D printed case.**
- Pogo Pins (Optional for specific supported PCBs) [\[More Info\]](001-‘’Cheese‘’/POGOPIN%20purchase%20Link.txt)
- Soldering Iron/Station 

    

## 3D Printing for SlimeVR-CheeseCake

This repository contains various 3D printed components required to assemble the SlimeVR-CheeseCake. Below are the necessary files and instructions.

### CheeseCake Case
- **Main Case**: [CheeseCake Case with AUX](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/004-3D%20Print%20Model/001.2-Chocolate-Case-With-AUX.stl) - Recommended design compatible with any 3D filament.
- **Alternative Designs**:
  - [Case with USB Port Only](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/004-3D%20Print%20Model/001.3-Chocolate-Case_TypeC-Only.stl)
  - [Case with Pogo Pins Cutout](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/004-3D%20Print%20Model/001.1-Chocolate-Case.stl)    
  - [Case for Knurled Insert Nuts](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/004-3D%20Print%20Model/001.4-Chocolate-Case_Type-C-only_insert-nuts.stl)
    - Size of Knurled Insert Nut is `M2*5*3.5 ( M2xOD3.5, 5mm Length )` like [This](https://www.aliexpress.us/item/1005004431154591.html)
    - No pogo pins cutout or AUX cutout, for new designs.
- If you want a larger battery, you can use the [803040-case](https://github.com/Sorakage033/SlimeVR-CheeseCake/tree/main/004-3D%20Print%20Model/000.1-Blue-Compact-Case-For-803040-Bat) modified by Blu3u.

### Top Lid
- **3D Printed Option**: [3D Printed Top Lid](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/004-3D%20Print%20Model/002-Cake-Top.stl)
- Note: Use elephant foot compensation to reduce fitting issues.
- **Acrylic Option**: For a 4mm transparent acrylic lid, use the dimensions provided in [this file](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/004-3D%20Print%20Model/AcrylicTop-CutSize-Thickness4mm.png).

### Essential Component
- **Switch Component**: [Switch for Case](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/004-3D%20Print%20Model/003-SW.stl) - This part is crucial for the assembly.
- Note: If it's hard to assemble, you can try narrowing the switch by scaling down the Z-axis.

### Holders (Recommended to Print in PETG Filament)
- [Clamp Holder](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/004-3D%20Print%20Model/004-''CLAMP''Holder.stl) - Fits 4cm and 3cm straps.
- [Clamp Holder 5cm Strap](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/004-3D%20Print%20Model/004-2-''CLAMP''Holder-5cm.stl) - Fits 5cm straps.
- [GoPro Chest Harness Compatible Clamp Holder](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/004-3D%20Print%20Model/004-1-''CLAMP''GoPro_Holder.stl) - For GoPro chest harness compatibility.
- [Slide Holder](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/004-3D%20Print%20Model/005-''SLIDE''Holder.stl) - Fits 4cm and 3cm straps.
- [Slide Holder 5cm Strap](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/004-3D%20Print%20Model/005-1-''SLIDE''Holder-5cm.stl) - Fits 5cm straps.

### Charging Dock (Recommended to Build the Type-C ChargeDock)
- **8-Tracker Type-C ChargeDock**     
  <img decoding="async" src="https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/999-PictureFiles/Intro_Type-c%20Charging%20Dock.png?raw=true" width="40%">
  - [Top Part](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/004-3D%20Print%20Model/ChargeDock-8port-Typec-Top.stl)
  - [Bottom Part](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/004-3D%20Print%20Model/ChargeDock-8port-Typec-Bottom.stl)
- **8-Tracker ChargeDock**:
  - [Top Part](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/004-3D%20Print%20Model/ChargeDock-8port-Top-Optimized.stl)
  - [Bottom Part](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/004-3D%20Print%20Model/ChargeDock-8port-Bottom-Optimized.stl)
- **6-Tracker ChargeDock**:
  - [Top Part](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/004-3D%20Print%20Model/ChargeDock-6port-Top.stl)
  - [Bottom Part](https://github.com/Sorakage033/SlimeVR-CheeseCake/blob/main/004-3D%20Print%20Model/ChargeDock-6port-Bottom.stl)

## Assembly    
    
1.  Apply about 2cm foam tape on the inner side of the case. Install two M2*7mm hexagonal spacers (either with a HAMMER, or push the spacer into the hole with a soldering iron to melt it in place)      
<img decoding="async" src="https://raw.githubusercontent.com/Sorakage033/SlimeVR-CheeseCake/main/999-PictureFiles/A-01.png" width="80%">     
2.  Place the switch part in position and affix the battery to the case.
<img decoding="async" src="https://raw.githubusercontent.com/Sorakage033/SlimeVR-CheeseCake/main/999-PictureFiles/A-02.png" width="80%">    
3.  Bend the battery wire to ensure it can be tucked into the reserved gap during installation.    
<img decoding="async" src="https://raw.githubusercontent.com/Sorakage033/SlimeVR-CheeseCake/main/999-PictureFiles/A-03.png" width="80%">    
4.  When installing the PCB, put the switch to the "UP" position, tilt it towards the side with the switch. Fit it into the reserved slot on the 3d printing part. It is extremely easy to break this switch!    
<img decoding="async" src="https://raw.githubusercontent.com/Sorakage033/SlimeVR-CheeseCake/main/999-PictureFiles/A-04.png" width="80%">    
5.  Tilt the board slightly towards the USB-C side, push the PCB at the side away from the switch.    
<img decoding="async" src="https://raw.githubusercontent.com/Sorakage033/SlimeVR-CheeseCake/main/999-PictureFiles/A-05.png" width="80%">     
6.  Press the whole PCB at position, screw on M2*5mm screws and pressure fit the cover.      
      
## Dock Assembly    

1.  Install M2*7mm hexagonal spacers into chargedock top piece. (either with a HAMMER, or push the spacer into the hole with a soldering iron to melt it in place).
3.  Insert PCB into chargedock bottom.
4.  Press the chargedock bottom into position, screw on M2*5mm screws.

## Support
If this project can help you I would be very happy!      
And also, if you want to give me some support, you can support me on [BOOTH](https://sorakage033.booth.pm/items/4859476)!
