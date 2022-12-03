# Soldering Guide
Soldering/Putting the PCB together is pretty simple, since there are not so many steps.

## Step 1 - SMD components
Start by soldering on the all SMD components first. 
These at least include five capacitors, a single LED and a single resistor.
The capacitors are soldered on the pads named `C1`, `C2`, `C3`, `C4` and `C5`. The resistor is soldered to pad `R7` and the LED to pad `D4`.

If you opted for the extra output components you will also have to solder six more resistors and three LEDs in this step.
The resistors are soldered on to the pads named `R1`, `R2`, `R3`, `R4`, `R5` and `R6`. The LEDs are soldered to the pads `D1`, `D2` and `D3`.

Your PCB should now look something like this:
![PCB](https://github.com/enwi/RNGBridgeDoc/blob/v2/images/smd_soldered.png)

## Step 2 - MAX3232 and transistors
Next push the MAX3232 IC into holes marked as `U1` on the PCB.
Make sure that the notch of the IC is aligned with the one printed on the PCB.
Then turn the PCB around and solder it in from the bottom.

If you opted for the extra output components you will also have to push the three transistors into the holes marked `Q1`, `Q2` and `Q3`.
Also make sure that the shape of the housing matches the one printed on the PCB.
Then turn the PCB around and solder them in from the bottom.
After that break or snip off the legs of the transistors.

Your PCB should now look something like this:
![PCB](https://github.com/enwi/RNGBridgeDoc/blob/v2/images/thd_soldered.png)

## Step 3 - Connectors
Take the three pin socket strip and push it into the holes marked `J2` on the PCB.
Turn the PCB around and solder it in from the bottom.

Repeat above steps for two socket strips of the ESP (Note these are only included if you opted for the ESP8266).
Note that these go into the holes inside of the outline of the ESP8266 D1 Mini an NOT into the holes marked as `J3` and `J4`.

Now is also a good time to solder two of the pin headers onto the ESP8266 D1 Mini.

If you opted for the extra output components you will also have to push the three terminal block recepticles into the holes marked as `J5`, `J6` and `J7`.
Turn the PCB around and solder them in from the bottom.
Tip: solder these recepticles before soldering the scoket strips, it will be easier.

Your PCB should now look something like this:
![PCB](https://github.com/enwi/RNGBridgeDoc/blob/v2/images/connectors_soldered.png)

## Step 4 - RJ12
Take the RJ12 connector and push it into the holes marked as `J1` on the PCB.
Turn the PCB around and solder it in from the bottom.

Your PCB should now look something like this:
![PCB](https://github.com/enwi/RNGBridgeDoc/blob/v2/images/rj12_soldered.png)

## Step 5 - Power and ESP8266
RNGBridge can be powered either by the charge controller (using the optional buck converter) or through the USB of the ESP8266 D1 Mini.

> Note that you can ONLY have RNGBridge powered by EITHER the buck converter OR the USB. Connecting BOTH at the SAME time can lead to BOTH RNGBridge and/or your charge controller being destroyed!

For powering RNGBridge by the charge controller, plug in the buck converter into the socket strip marked as `J2`.
It should look something like this:
![PCB](https://github.com/enwi/RNGBridgeDoc/blob/v2/images/rj12_powered.png)

For powering RNGBridge by USB, plug in a USB to the ESP8266 D1 Mini.
It should look something like this:
![PCB](https://github.com/enwi/RNGBridgeDoc/blob/v2/images/usb_powered.png)

If everything went according to plan, then your PCB should now look something like this:
![PCB](https://github.com/enwi/RNGBridgeDoc/blob/v2/images/complete.png)

## Step 6 - Commissioning
Get an RJ12 cable ready and continue with the [Commissioning Guide](https://github.com/enwi/RNGBridgeDoc/blob/v2/comissioning.md).