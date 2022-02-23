# Soldering Guide
Soldering/Putting the PCB together is pretty simple, since there are not so many steps.

## Step 1 - Capacitors
Start by soldering on the 5 small capacitors first. These go on the pads with the names `C1`, `C2`, `C3`, `C4` and `C5`.

Then continue with the bigger capacitor and solder it on the pad `C6`.

## Step 2 - MAX3232
Next push the MAX3232 IC into the PCB, turn the PCB around and solder it in from the bottom.

> It should go in the spot which is marked as `U1`.
> Make sure that the notch of the IC macthes with the one printed on the PCB.

## Step 3 - Connectors
Take the two socket strips, push them into the PCB, turn the PCB around and solder them in from the bottom.

## Step 4 - RJ12
Take the RJ12 connector and push it into the PCB, turn the PCB around and solder it in from the bottom.

Your PCB should now look like this:
![PCB](https://github.com/enwi/RNGBridgeDoc/blob/master/images/soldering.png)

## Step 5 - Power and ESP8266
Take the power converter and plug it into the 3 pin socket strip (it should only go in one way).

Then take the ESP8266 and plug it into the 2x4 pin socket strip.
Make sure that the antenna and the body of the ESP8266 are aligned in the direction of the arrow on the PCB. 

> In other words the ESP8266 should NOT be over top of the MAX3232, but off to the side of the PCB.

If everything went according to plan, then your PCB should now look like this:
![PCB](https://github.com/enwi/RNGBridgeDoc/blob/master/images/finished.png)

## Step 6 - Plug it in
Get an RJ12 cable and connect `RNG to WiFi` to your Renogy charge controller.

You can continue with the [Commissioning Guide](https://github.com/enwi/RNGBridgeDoc/blob/master/comissioning.md)