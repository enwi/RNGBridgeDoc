# Debugging
If you need to debug `RNGBridge` or want to see what's going on under the hood, first you will need a Serial to USB converter.
Hook its RX/receiver pin up to pin D4 of the ESP8266 D1 mini and open a serial terminal of your choice.
Make sure you set the baudrate to `115200` and start the terminal.
Now you should be able to see every debug output in your terminal.

> The specific serial options are `115200 8N1`, which stands for a baudrate of `115200`,
> 8 data bits, no parity and 1 stop bit.