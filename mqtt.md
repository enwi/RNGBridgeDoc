# MQTT
`RNGBridge` can publish the data read from your Charge Controller to a local MQTT Broker, thus making it accessible to other devices or home automation systems.
It supports credentials so you can also connect to secured MQTT Brokers.

## Setup
1. Open the settings menu by clicking the gear icon in the top right of the page.
2. Click on the panel named `MQTT`.
3. Enable `MQTT`.
4. Enter the MQTT Broker IP e.g. `192.168.2.2` in the `Server` field.
5. Optionally enter the MQTT Broker port e.g. `1883` in the `Port` field (default is 1883 so if you are using the same port you can skip this step).
6. Optionally enter the MQTT client identifier used by `RNGBridge` in the `Id` field.
7. Optionally enter the MQTT Broker username in the `User` field.
8. Optionally enter the MQTT Broker password in the `Password` field.
9. Enter the MQTT Topic where `RNGBridge` should publish the data e.g `/solar/rng` (default is `/rng`).
10. If you verified your settings press the `SAVE MQTT CONFIG` button.
11. `RNGBridge` will reboot and try to connect to the MQTT Broker and displays the status on the settings page.

> Note that due to the limited resources of the ESP8266 only Brokers without TLS/SSL are supported for now

<img src="https://github.com/enwi/RNGBridgeDoc/blob/main/images/gif/mqtt.gif" width="600">

## Troubleshooting
### Status field shows `Could not connect` or `Disconnected`
- Verify your configuration and press the `SAVE MQTT CONFIG` button if you made changes.
- Verify your MQTT Broker is reachable (e.g. with `MQTT Explorer`)
- Wait a minute and check if the status changed
- If you still have issues get help on my discord server by clicking on this icon -> [![Discord](https://img.shields.io/discord/781219798931603527.svg?label=enwi&logo=discord&logoColor=ffffff&color=7389D8&labelColor=6A7EC2)](https://discord.gg/YxVyJWX62h)

## Data Structure
The current Charge Controller data is sent every 2 seconds and is provided as a JSON object as follows:
```
{
  "device" : "0123456789AB",
  "b" :
  {
    "charge" : 100,
    "voltage" : 13.5,
    "current" : 1.45,
    "temperature" : 25.0
  },
  "l" :
  {
    "voltage" : 13.5,
    "current" : 1.56,
    "power" : 21
  },
  "p" :
  {
    "voltage" : 32.6,
    "current" : 5.45,
    "power" : 177
  },
  "s" :
  {
    "state" : 2,
    "errorState" : 0,
    "temperature" : 25.5
  }
}
```

### Data values
| Object/Variable | Type   | Value             | Description                                  |
|:----------------|--------|-------------------|----------------------------------------------|
| device          | String | e.g. 0123456789AB | Device identifier, MAC address of ESP        |
| b               | Object | -                 | JSON object containing battery data          |
| charge          | Number | 0 - 100           | Battery charge in %                          |
| voltage         | Float  | 0.0 - XX.X        | Battery voltage in Volts                     |
| current         | Float  | 0.0 - XX.X        | Battery current in Ampere                    |
| temperature     | Float  | 0.0 - XX.X        | Battery temperature in degrees C             |
| l               | Object | -                 | JSON object containing load data             |
| voltage         | Float  | 0.0 - XX.X        | Load voltage in Volts                        |
| current         | Float  | 0.0 - XX.X        | Load current in Ampere                       |
| power           | Number | 0 - XXXX          | Load power in Watts, note multiplying voltage with current gives you a more accurate value as this is the value returned by the charge controller |
| p               | Object | -                 | JSON object containing solar panel data      |
| voltage         | Float  | 0.0 - XX.X        | Solar panel voltage in Volts                 |
| current         | Float  | 0.0 - XX.X        | Solar panel current in Ampere                |
| power           | Number | 0 - XXXX          | Solar panel power in Watts, note multiplying voltage with current gives you a more accurate value as this is the value returned by the charge controller |
| s               | Object | -                 | JSON object containing controller state data |
| state           | Number | 0 - 6             | Charge controller state, mode of operation   |
| errorState      | Number | 0 - 33488896      | Charge controller error state                |
| temperature     | Float  | 0.0 - XX.X        | Charge controller temperature in degrees C   |

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
On connection to the MQTT Broker `RNGBridge` will send a connection message which indicates that the device is online. This message is being retained as long as the connection to the Broker stays alive. If `RNGBridge` is being disconnected due to different reasons the broker will send a last will message. This disconnect message is also being retained. So whenever another client subscribes to the topic it will be notified on whether `RNGBridge` is online or offline.

### Connect message
```
{
  "device" : "0123456789AB",
  "connected" : true
}
```

### Disconnect message
```
{
  "device" : "0123456789AB",
  "connected" : false
}
```
