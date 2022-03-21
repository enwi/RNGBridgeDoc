# Automatic Load and Output (`Out1`, `Out2`, `Out3`) control
`RNGBridge` can automatically control the load output of the charge controller as well as three customizable outputs namely `Out1`, `Out2` and `Out3`.
Each output (`Load`, `Out1`, `Out2` and `Out3`) can have indivual settings that are fully customizable. The outputs `Out1`, `Out2` and `Out3` also feature a status LED, which will be lit if the respective output is active/on.

The settings consist of a `control input`, a lower and upper setpoint and an inversion flag.
The `control input` defines by which value (provided by the charge controller) the output should be controlled.
You can choose between:
- `Battery SOC` (Current state of charge ranging from 0% (battery empty) to 100% (battery fully charged))
- `Battery Voltage` (Current battery voltage ranging from 0.0V to ~48.0V)

The lower setpoint defines when the output should be turned off if the `control input` falls below this threshold (`control input` `<` lower setpoint).
The upper setpoint defines when the output should be turned on if the `control input` is equal to or larger than this threshold (`control input` `>=` upper setpoint).
The inversion flag inverts the behaviour of the lower and upper setpoints.

For example if you want the `Load` to turn on when the battery is almost fully charged (e.g. at 90% SOC) and then discharge the battery until it is half charged (50% SOC) then you would set `control input` to `Battery SOC`, the lower setpoint to 51% and the upper setpoint to 90%.
The inversion flag should be turned off.
An example is shown in the below image

<img src="https://github.com/enwi/RNGBridgeDoc/blob/main/images/control_example1.png" width="600">

## Controlling a relay using `Out1`, `Out2` or `Out3`
The outputs `Out1`, `Out2` and `Out3` are open collector outputs that you can hook stuff up to with a voltage of up to 24V.
Open collector means that the collector of the NPN transistor is available on the left pin of the connector and ground on the other.
Here is an image to show the outputs.

<img src="https://github.com/enwi/RNGBridgeDoc/blob/main/images/output.png" width="600">

The open collector output can be used to control devices or loads that have a higher operating voltage or need higher currents than `RNGBridge` can provide.
A simple example is to control a 12V device using a relay.
A relay is needed, because the open collector output can only control loads of up to 24V and 500mA.
In this case you can use a 5V (e.g. SRD-05VDC-SL-C), 12V (e.g. SRD-12VDC-SL-C) or even 24V (e.g. SRD-24VDC-SL-C) relais or anything in between.
You will also need to provide a 5V, 12V or 24V power supply respectively to be able to control your relay (This will most likely be provided by your solar system).
You can then connect one wire of the relay coil to your positive terminal (anode, +) of the power supply and the other wire of the relay coil to the open collector of `RNGBridge`.
The negative terminal (cathode, -) of the power supply will be connected to the ground of `RNGBridge`.
Then hook up your load to the normally closed (NC) and common (C) or normally open (NO) and common (C) connections of the relay.
Now you can control a load using a relais connected to `RNGBridge`.