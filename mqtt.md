# MQTT
`RNG to WiFi` can publish the data read from your Charge Controller to a local MQTT Broker, thus making it accessible to other devices or home automation systems.
It supports credentials so you can also connect to secured MQTT Brokers.

## Setup
1. Go to the MQTT tab
2. Enter the MQTT Broker ip e.g. `192.168.2.16` in the `Broker IP` field
3. Enter the MQTT Broker port e.g. `1883` in the `Broker Port` field (default is 1883 so if you are using the same port you can skip this step)
4. Enter the MQTT Topic where `RNG to WiFi` should publish the data e.g `/solar/rng` (default is `/rng`)
5. Optionally enter the MQTT username and password if you use a password protected MQTT Broker (default is no credentials)
6. Enable the MQTT service by enabling the `Enable` switch
7. Watch the `Status` field, it should display `Connected` if everything went according to plan

> Note that due to the limited resources of the ESP8266 only Brokers without TLS/SSL are supported for now

## Troubleshooting
### Status field shows `IP wrong`
Verify that you entered the correct IP address or reload the site and try again.

### Status field shows `Port wrong`
Verify that you entered the correct port or reload the site and try again.

### Status field shows `IP and Port wrong`
Verify that you entered the correct IP address and port or reload the site and try again.

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
On connection to the MQTT Broker `RNG to WiFi` will send a connection message which indicates that the device is online. This message is being retained as long as the connection to the Broker stays alive. If `RNG to WiFi` is being disconnected due to different reasons the broker will send a last will message. This disconnect message is also being retained. So whenever another client subscribes to the topic it will be notified on whether `RNG to WiFi` is online or offline.

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
