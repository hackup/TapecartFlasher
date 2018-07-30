# TapecartFlasher #

TapecartFlasher is a Windows tool to write and read out 
C64 Tapecart modules directly from the PC via an Arduino
UNO or NANO.

[a tape port storage pod for the C64](https://github.com/ikorb/tapecart)

At the first use of the Arduino, the Arduino software can
be uploaded from TapecartFlasher to the Ardunio.
Each connection ("Connect") with the Arduino will check if
the Arduino software is up to date.
The Arduino development environment is not needed for this.
The hex files for your Arduino board must exist in same directory
as the TapecartFlasher.exe file.

# Procedure for writing or reading a TCRT file: #

1. Connect the Tapecart module to the Arduino via an adapter.

Wiring (Arduino <-> Tapecart):
```
Arduino ! Tapecart
------------------
GND     ! GND
+5V     ! + 5V
Pin D2  ! MOTOR
Pin D3  ! READ
Pin D4  ! WRITE
Pin D5  ! SENSE
```

2. Connect the Arduino via USB to the PC

3. Please check if the Arduino is properly recognized by Windows
and appears as a COM port in Device Manager. You may still need to 
ensure that the correct Arduino USB driver is installed.

4. Start Windows TapecartFlasher tool.

5. Click "Detect". If the Arduino already has a TapecartFlasher
Software, the COM port should by found and displayed.

6. If the Arduino does not yet contain the TapecartFlasher software,
select the correct COM port, click on "Upload / Update Sketch", choose
the correct Arduino board and click Update. The software will now be
transferred to the Arduino. Close the update window and click "Detect" 
again and the correct COM port should be displayed.

7. Click "Connect". After a few seconds, some information about the connected
Tapecart module will be displayed.

8. With the "Write" or "Read" button a TCRT file can be transfered to or from the
Tapecart module.

In case of problems please contact feedback@dgerhardt.de or user detlef at 
forum64.de.

Have fun.

# Credits #

This software uses the [ArduinoSketchUploader Library](https://github.com/christophediericx) by Christophe Diericx.

