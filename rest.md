# REST API
With the REST API you can control the outputs as well as request the current state of the charge controller and the outputs.

## Control outputs `Load`, `Out1`, `Out2` and `Out3`
For controlling the outputs you have to send a `POST`, `PUT` or `PATCH` request to the endpoint `/api/control` containing a JSON body with the desired state.
To turn the load output on the body needs to contain `{"load":true}`, to turn it off `{"load":false}`.
For the three control outputs this is done in a similar manner.
To turn on `Out1` the body needs to contain `{"out1":true}`, to turn it off `{"out1":false}`.
The same applies to `Out2` (on: `{"out2":true}`, off: `{"out2":false}`) and `Out3` (on: `{"out3":true}`, off: `{"out3":false}`)
You are also able to control multiple outputs at the same time.
For example the following body will turn on the `Load` and `Out2` and at the same time turn off `Out1` and `Out3`:
`{"load":true,"out2":true,"out3":false,"out1":false}`.

You can also try this using `curl` for that replace the placeholer `IP` with the ip address of `RNGBridge`:
```shell
curl -X POST -H "Content-Type: application/json" -d '{"load":true}' IP/api/control
```
```shell
curl -X POST -H "Content-Type: application/json" -d '{"load":true,"out2":true,"out3":false,"out1":false}' IP/api/control
```

> Note if you have setup automatic control of the load output, out1, out2 or out3 you might be able to change the state of the output using the REST interface, but it will probably be overwritten by the automatic control in the next update cycle.
> So make sure that automatic control is disabled if you want to use this feature.

## Requesting controller state
For getting the state of the charge controller you have to send a `GET` request to the endpoint `/api/state`.
`RNGBridge` will then return a current state JSON object similar to the one returned with [MQTT](https://github.com/enwi/RNGBridgeDoc/blob/main/mqtt.md).
If wanted the MQTT obect could be extended to also have these values included.

### Data Structure
```json
{
    "mqttsta": "Connected",
    "otasta": "2.7.0",
    "pvosta": "Disabled",
    "b": {
        "ch": 79,
        "vo": 12.11761,
        "cu": 8.252449,
        "te": 18
    },
    "l": {
        "vo": 12.11761,
        "cu": 0
    },
    "p": {
        "vo": 13.9,
        "cu": 7.194245
    },
    "c": {
        "st": 1,
        "er": 0,
        "te": 19
    },
    "o": {
        "l": false,
        "o1": false,
        "o2": false,
        "o3": false
    },
    "up": 80,
    "he": 38008
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
| mqttsta         | Bool   | String            | Current human readable state of the MQTT module of `RNGBridge` |
| otasta          | Bool   | String            | Latest available version number of `RNGBridge`, only present if a software update is available |
| pvosta          | Bool   | String            | Current human readable state of the PVOutput module of `RNGBridge` |
| up              | Bool   | Number            | Uptime in seconds                            |
| he              | Bool   | Number            | Current heap usage in bytes                  |

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