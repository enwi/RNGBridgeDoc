# MQTT
`RNGBridge` can publish the data read from your Charge Controller to a local MQTT Broker, thus making it accessible to other devices or home automation systems.
It supports credentials so you can also connect to secured MQTT Brokers.
Since ([V2.7.0](https://github.com/enwi/RNGBridgeDoc/releases/tag/2.7.0)) `RNGBridge` can also automatically integrate itself into Homeassistant using [Homeassistant Discovery](https://www.home-assistant.io/docs/mqtt/discovery/).

## Setup
1. Open the settings menu by clicking the gear icon in the top right of the page.
2. Click on the panel named `MQTT`.
3. Enable `MQTT`.
4. Enter the MQTT Broker IP e.g. `192.168.2.2` in the `Server` field.
5. Optionally enter the MQTT Broker port e.g. `1883` in the `Port` field (default is `1883` so if you are using the same port you can skip this step).
6. Optionally enter the MQTT client identifier used by `RNGBridge` in the `Id` field.
7. Optionally enter the MQTT Broker username in the `User` field.
8. Optionally enter the MQTT Broker password in the `Password` field.
9. Enter the MQTT base topic where `RNGBridge` should publish the data e.g `/solar/rng` (default is `/rng`).
10. Optionally enter the MQTT update interval in seconds in the `Update interval (seconds)` field.
11. Optionally enable Homeassistant Discovery and control `RNGBridge` directly through Homeassistant.
12. Optionally enter the Homeassistant Discovery Topic in the field `Discovery Topic` (default is `homeassistant`, which is also the default of the [MQTT Integration](https://www.home-assistant.io/integrations/mqtt/)).
13. If you verified your settings press the `SAVE MQTT CONFIG` button.
14. `RNGBridge` will reboot and try to connect to the MQTT Broker and displays the status on the settings page.

> Note that due to the limited resources of the ESP8266 only Brokers without TLS/SSL are supported for now

<img src="https://github.com/enwi/RNGBridgeDoc/blob/main/images/gif/mqtt.gif" width="600">

## Troubleshooting
### Status field shows `Could not connect` or `Disconnected`
- Verify your configuration and press the `SAVE MQTT CONFIG` button if you made changes.
- Verify your MQTT Broker is reachable (e.g. with `MQTT Explorer`)
- Wait a minute and check if the status changed
- If you still have issues get help on my discord server by clicking on this icon -> [![Discord](https://img.shields.io/discord/781219798931603527.svg?label=enwi&logo=discord&logoColor=ffffff&color=7389D8&labelColor=6A7EC2)](https://discord.gg/YxVyJWX62h)

## Data Structure
The current Charge Controller data is sent at the configured interval and is published under the subtopic `/state` as a JSON object as follows:
```json
{
    "b": {
        "ch": 100,
        "vo": 13.5,
        "cu": 1.45,
        "te": 25.0
    },
    "l": {
        "vo": 13.5,
        "cu": 1.56,
        "po": 21
    },
    "p": {
        "vo": 32.6,
        "cu": 5.45,
        "po": 177
    },
    "c": {
        "st": 2,
        "er": 0,
        "te": 25.5
    },
    "o": {
        "l": true,
        "o1": false,
        "o2": true,
        "o3": false
    }
}
```

### Data values
| Object/Variable | Type   | Value             | Description                                  |
|:----------------|--------|-------------------|----------------------------------------------|
| b               | Object | -                 | JSON object containing battery data          |
| ch              | Number | 0 - 100           | Battery charge in %                          |
| vo              | Float  | 0.0 - XX.X        | Battery voltage in Volts                     |
| cu              | Float  | 0.0 - XX.X        | Battery current in Ampere                    |
| te              | Float  | 0.0 - XX.X        | Battery temperature in degrees C             |
| l               | Object | -                 | JSON object containing load data             |
| vo              | Float  | 0.0 - XX.X        | Load voltage in Volts                        |
| cu              | Float  | 0.0 - XX.X        | Load current in Ampere                       |
| po              | Number | 0 - XXXX          | Load power in Watts, note multiplying voltage with current gives you a more accurate value as this is the value returned by the charge controller |
| p               | Object | -                 | JSON object containing solar panel data      |
| vo              | Float  | 0.0 - XX.X        | Solar panel voltage in Volts                 |
| cu              | Float  | 0.0 - XX.X        | Solar panel current in Ampere                |
| po              | Number | 0 - XXXX          | Solar panel power in Watts, note multiplying voltage with current gives you a more accurate value as this is the value returned by the charge controller |
| c               | Object | -                 | JSON object containing controller state data |
| st              | Number | 0 - 6             | Charge controller state, mode of operation   |
| er              | Number | 0 - 33488896      | Charge controller error state                |
| te              | Float  | 0.0 - XX.X        | Charge controller temperature in degrees C   |
| o               | Object | -                 | JSON object containing output states         |
| l               | Bool   | true/false        | Charge controller load output enabled(true) or disabled(false) |
| o1              | Bool   | true/false        | RNGBridge `Out1` enabled(true) or disabled(false) |
| o2              | Bool   | true/false        | RNGBridge `Out2` enabled(true) or disabled(false) |
| o3              | Bool   | true/false        | RNGBridge `Out3` enabled(true) or disabled(false) |

#### state values
- 0: charging deactivated
- 1: charging activated
- 2: mppt charging mode
- 3: equalizing charging mode
- 4: boost charging mode
- 5: floating charging mode
- 6: current limiting (overpower)

#### errorState values
- B31: Reserved
- B30: Charge MOS short circuit
- B29: Anti-reverse MOS short circuit
- B28: Solar panel reversly connected
- B27: Solar panel working point over-voltage
- B26: Solar panel counter current
- B25: Photovoltaic input side over voltage
- B24: Photovoltaic input side short circuit
- B23: Photovoltaic input overpower
- B22: Ambient temperature too high
- B21: Controller temperature too high
- B20: Load overpower or load over-current
- B19: Load short circuit
- B18: Battery under-voltage warning
- B17: Battery over-voltage
- B16: battery over-discharge
- B0-B15: Reserved

BXX indicates the bit of the number

## Other messages
On connection to the MQTT Broker `RNGBridge` will send a connection message to the subtopic `/lwt` which indicates that the device is online.
This message is being retained as long as the connection to the Broker stays alive.
If `RNGBridge` is being disconnected due to different reasons the broker will send a last will message.
This disconnect message is also being retained.
So whenever another client subscribes to the topic it will be notified on whether `RNGBridge` is online or offline.

### Connect message
```
Connected
```

### Disconnect message
```
Disconnected
```

## Controlling `Load`, `Out1`, `Out2` and `Out3`
Since ([V2.7.0](https://github.com/enwi/RNGBridgeDoc/releases/tag/2.7.0)) it is possible to control the outputs of RNGBridge with MQTT.
To turn a specific output on or off you can publish a message containing either `true` or `false` to the subtopics `/ol`, `/o1`, `/o2` and `/o3`,
of the MQTT base topic configured in step 9.
So with the default MQTT base topic being `/rng`, you would need to publish a message to `/rng/ol`, `/rng/o1`, `/rng/o2` and `/rng/o1`.
