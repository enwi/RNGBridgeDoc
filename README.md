[![Discord](https://img.shields.io/discord/781219798931603527.svg?label=enwi&logo=discord&logoColor=ffffff&color=7389D8&labelColor=6A7EC2)](https://discord.gg/YxVyJWX62h)

# RNGBridgeDoc V2
Documentation and guides for RNGBridge V2, an RS232 to WiFi bridge for Renogy solar charge controllers with PVOutput and MQTT support
<!-- ![pcb](https://github.com/enwi/RNGBridgeDoc/blob/main/images/populated_pcb.jpg) -->

## Feature overview
- Beautiful web interface
   - Control load output remotely
   - Get more information about system errors by hovering over them
   - Battery capacity intuitively visualized
   - ![web interface](https://github.com/enwi/RNGBridgeDoc/blob/main/images/webinterface.png)
- Over the air software updates (`OTA`)
   - Keeps configuration after update
- Optional data publishing to [MQTT](https://en.wikipedia.org/wiki/MQTT)
   - Works with protected Brokers (`username`, `password`)
   - Configurable `topic`, `client id`, `port` and `ip`
- Optional data publishing to [PVOutput](https://pvoutput.org)
   - Configurable time offset
- Automatic load, out1, out2 and out3 control
   - lower/upper setpoint
   - can be inverted
   - control depending on battery SOC(state of charge) or battery voltage
- Control load output via [REST api](https://github.com/enwi/RNGBridgeDoc/blob/main/rest.md)

Missing anything? If you want support for a custom feature or want to suggest something, feel free to open an issue or join the [Discord Server](https://discord.gg/YxVyJWX62h).

## Where to buy
You can get [this kit](https://www.tindie.com/products/21360/) on my [tindie store](https://www.tindie.com/stores/enwi/#store-section-products)

## Supported devices
All supported and tested Charge Controllers can be found [here](https://github.com/enwi/RNGBridgeDoc/blob/main/controllers.md)

## Getting started
- [Assemble `RNGBridge` using the build instructions](https://github.com/enwi/RNGBridgeDoc/blob/main/soldering.md)
- [Setup your device have using the commissioning guide](https://github.com/enwi/RNGBridgeDoc/blob/main/comissioning.md)
- [Control load output through REST api](https://github.com/enwi/RNGBridgeDoc/blob/main/rest.md)
- [Connect `RNGBridge` to your MQTT Broker](https://github.com/enwi/RNGBridgeDoc/blob/main/mqtt.md)
- [Publishing data to PVOutput](https://github.com/enwi/RNGBridgeDoc/blob/main/pvoutput.md)

## About
See the about section [here](https://github.com/enwi/RNGBridgeDoc/blob/main/about.md)
