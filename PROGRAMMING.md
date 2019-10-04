UPDuino v2.0 Device Programming

Hardware Needed:
* (Gnarly Grey UPDuino v2.0 Board)[http://gnarlygrey.atspace.cc/development-platform.html#upduino_v2]
Software Needed:
    • (Lattice Diamond Programmer Standalone (v3.9 x64 used for programming instructions))
        [http://www.latticesemi.com/en/Products/DesignSoftwareAndIP/ProgrammingAndConfigurationSw/Programmer.aspx#_20C94305815A4B3AAAFEA8B83943B751]
    • (Lattice iCECube2 Software) [http://www.latticesemi.com/Products/DesignSoftwareAndIP/FPGAandLDS/iCEcube2.aspx#_4351BE10BA504435B5226390CF5D7D4C]
FPGA Projects Needed:
    • (UPDuino Blinky LED Design)[http://www.gnarlygrey.com/downloads/RGB_LED_BLINK_20170606.tar]
Programming (SPI Flash):
1. Plug UPDuino v2.0 in to your PC using the micro USB port on the board
2. Open Lattice Diamond Programmer
3. Click ‘Detect Cable’ then ‘OK’
4. After scanning select ‘Generic JTAG Device’ and ‘Select iCE40 UltraPlus’
5. Under ‘Device’ click iCE40UP3K and change it to iCE40UP5K
6. Under ‘Operation’ double click ‘Fast Program’ and change ‘Access Mode:’ to ‘SPI Flash Programming’
7. Select your *.hex programming file under ‘Programming file’.
8. Configure the following ‘SPI Flash Options’
    a. Numonyx
    b. SPI-N25Q032
    c. 8-pin VDFPN8
9. Click ‘Load from File’ under ‘SPI Programming’ to get load size
10. Click ‘Design’’Program’

Project Synthesis (Compiling) and bitstream (Firmware) generation:
1. Unzip RGB_LED_BLINK_20170606.zip
2. Open Lattice iCECube2 Software
3. Double click ‘Open Project’
4. Navigate to *\RGB_LED_BLINK_20170606\rgb\rgb_sbt.project and ‘Open’
5. Double click ‘Run Synplify Pro Synthesis’
6. Right click on ‘Run P&R’ and left click ‘Run Bitmap’
    a. Note – this will run all remaining synthesis steps including place, route and bitmap generation.
    b. Generated bitstream will be loaded in the *\rgb\rgb_Implmnt\sbt\outputs\bitmap folder