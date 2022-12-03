# First comissioning of `RNGBridge`

## Step 1 - Connect `RNGBridge` to charge controller
Connect `RNGBridge` with an `RJ12` cable to your charge controllers `RS232` port. 
The orange status LED on `RNGBridge` will light up solid for a few seconds. 
Once the LED starts blinking at a 1 second interval you can continue with the next step.

> If the LED blinks on for 2 seconds and off for 1 second then there is a communication issue with your charge controller.
> Double check your wiring and make sure your device is supported as described in [Tested Controllers](https://github.com/enwi/RNGBridgeDoc/blob/main/controllers.md).
> If you still have issues get help on my discord server by clicking on this icon -> [![Discord](https://img.shields.io/discord/781219798931603527.svg?label=enwi&logo=discord&logoColor=ffffff&color=7389D8&labelColor=6A7EC2)](https://discord.gg/YxVyJWX62h)

## Step 2 - Connect to `RNGBridge` wifi
Connect your phone/tablet/pc to the WiFi network called `rngbridge` followed by a mix of 12 letters and numbers for example `rngbridge E8DB849C6FDF`

## Step 3 - Open user interface 
Once connected, your phone/tablet/pc should ask you to sign in to rngbridge (captive portal).
On Android you will need to click on the popup on other devices (iOS, MacOS) the captive portal will open automatically.
Once opened you are greeted with the user interface.

> On some devices this can take up to 30 seconds for the message to be displayed.

>If the captive portal does not open or no message is displayed you can alternatively type in the URL `192.168.4.1` and open the website (<a href="http://192.168.4.1" target="_blank">or click here</a>).
>After the page loaded, you are presented with the user interface of `RNGBridge`.

## Step 4 - Change device address
Depending on your charge controller or if you have configured it with the bluetooth module before
it might be needed to change the modbus device address `RNGBridge` uses to communicate with your charge controller.
One good indication for this is if the orange led stays lit for 2 seconds, turns off for 2 seconds and the data in the GUI is all zeros and does not change.
To change the address follow the follwing steps:

1. Open the settings menu by clicking the gear icon in the top right of the page.
2. Click on the panel named `Device`.
3. Enter the device address (1 - 255 where 255 is default) in the `Address` field
4. Click on `SAVE DEVICE CONFIG`

If you want to use `RNGBridge` as standalone aka in access point mode you are done with comissioning now. 
If you want to connect `RNGBridge` with your local WiFi network continue with step 5.

## Step 5 - Connect to WiFi network
1. Open the settings menu by clicking the gear icon in the top right of the page.
2. Click on the panel named `WiFi`.
3. select `Client` from the `WiFi mode` dropdown.
4. Enter the name of the WiFi network you want `RNGBridge` to connect with in the `SSID` field.
5. Enter the password of the WiFi network in the `Password` field.

DHCP is selected by default, meaning `RNGBridge` will get an IP assigned from your network router.
If you want to give it a static IP address or want to do some advanced configuration (`Netmask`, `Gateway`, `DNS`) disable DHCP and more options will appear.

Verify that your WiFi settings (`SSID`, `Password`, etc.) are correct and press the `SAVE WIFI CONFIG` button.
After that `RNGBridge` will reboot and try to connect to the WiFi network.
If it can't connect due to the WiFi not being available or the settings being invalid `RNGBridge` will fall back to the access point mode.

<img src="https://github.com/enwi/RNGBridgeDoc/blob/v2/images/gif/wifi_client.gif" width="600">

## Step 6 - Open user interface from local network device
Once `RNGBridge` has connected successfully with your local WiFi network you can access the user interface from all devices connected to you local network.
For that open a webbrowser and enter the IP address of `RNGBridge`.

> If you can't figure out the IP address you can connect a USB to serial converter to pin `D4` of the ESP8266 D1 Mini and open a terminal with `8N1` and `115200` baudrate.
> Then press the reset button of the ESP and the IP address will be printed to your console.

If everything worked out fine you are now setup. For infos on how to setup `MQTT` or `PVOutput` please take a look at the respective guides [MQTT](https://github.com/enwi/RNGBridgeDoc/blob/v2/mqtt.md) and [PVOutput](https://github.com/enwi/RNGBridgeDoc/blob/v2/pvoutput.md).
