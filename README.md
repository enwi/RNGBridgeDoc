[![Discord](https://img.shields.io/discord/781219798931603527.svg?label=enwi&logo=discord&logoColor=ffffff&color=7389D8&labelColor=6A7EC2)](https://discord.gg/YxVyJWX62h)

# RNGBridgeDoc V2
Documentation and guides for RNGBridge V2, an RS232 to WiFi bridge for Renogy solar charge controllers with PVOutput and MQTT support
<!-- ![pcb](https://github.com/enwi/RNGBridgeDoc/blob/main/images/populated_pcb.jpg) -->

## Feature overview
- Beautiful web interface
   - Control `Load`, `Out1`, `Out2` and `Out3` remotely
   - Get more information about system errors by hovering over them
   - Battery capacity intuitively visualized
   - ![web interface](https://github.com/enwi/RNGBridgeDoc/blob/main/images/webinterface.png)
- Over the air software updates (`OTA`)
   - Displays a banner with download link when a new update is available (since [V2.5.0](https://github.com/enwi/RNGBridgeDoc/releases/tag/2.5.0))
   - Keeps configuration after update
- Optional data publishing to [MQTT](https://en.wikipedia.org/wiki/MQTT)
   - Works with protected Brokers (`username`, `password`)
   - Configurable `topic`, `client id`, `port` and `ip`
   - Configurable update interval (since [V2.3.0](https://github.com/enwi/RNGBridgeDoc/releases/tag/2.3.0))
   - Control `Load`, `Out1`, `Out2` and `Out3` (since [V2.7.0](https://github.com/enwi/RNGBridgeDoc/releases/tag/2.7.0))
   - Supports [Homeassistant Discovery](https://www.home-assistant.io/docs/mqtt/discovery/) (since [V2.7.0](https://github.com/enwi/RNGBridgeDoc/releases/tag/2.7.0))
   - Publish data on individual topics (since [V2.10.0](https://github.com/enwi/RNGBridgeDoc/releases/tag/2.10.0))
- Optional data publishing to [PVOutput](https://pvoutput.org)
   - Configurable time offset
- Automatic `Load`, `Out1`, `Out2` and `Out3` control
   - lower/upper setpoint
   - can be inverted
   - control depending on battery SOC(state of charge), battery voltage, panel voltage (since [V2.6.0](https://github.com/enwi/RNGBridgeDoc/releases/tag/2.6.0)) or panel current (since [V2.6.0](https://github.com/enwi/RNGBridgeDoc/releases/tag/2.6.0))
- [REST API](https://github.com/enwi/RNGBridgeDoc/blob/main/rest.md)
   - Control `Load`, `Out1`, `Out2` and `Out3`
   - Request current charge controller state (since [V2.7.0](https://github.com/enwi/RNGBridgeDoc/releases/tag/2.7.0))

Missing anything? If you want support for a custom feature or want to suggest something, feel free to open an issue or join the [Discord Server](https://discord.gg/YxVyJWX62h).

## Where to buy
You can get [this kit](https://www.tindie.com/products/21360/) on my [tindie store](https://www.tindie.com/stores/enwi/#store-section-products)

## Supported devices
All supported and tested Charge Controllers can be found [here](https://github.com/enwi/RNGBridgeDoc/blob/main/controllers.md)

## Getting started
- [Assemble `RNGBridge` using the build instructions](https://github.com/enwi/RNGBridgeDoc/blob/main/soldering.md)
- [Setup your device using the commissioning guide](https://github.com/enwi/RNGBridgeDoc/blob/main/comissioning.md)
- [Connect `RNGBridge` to your MQTT Broker](https://github.com/enwi/RNGBridgeDoc/blob/main/mqtt.md)
- [Publishing data to PVOutput](https://github.com/enwi/RNGBridgeDoc/blob/main/pvoutput.md)
- [Automatically control load output and `Out1`, `Out2` and `Out3`](https://github.com/enwi/RNGBridgeDoc/blob/main/control.md)
- [Control `Load`, `Out1`, `Out2` and `Out3` through REST api](https://github.com/enwi/RNGBridgeDoc/blob/main/rest.md)
- [Request current charge controller state](https://github.com/enwi/RNGBridgeDoc/blob/main/rest.md)
- [Get debug output](https://github.com/enwi/RNGBridgeDoc/blob/main/debugging.md)

## About
See the about section [here](https://github.com/enwi/RNGBridgeDoc/blob/main/about.md)
