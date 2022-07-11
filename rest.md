# REST API
With the REST API you can control the `Load` output as well as the three control outputs `Out1`, `Out2` and `Out3`.
For that you have to send a `POST`, `PUT` or `PATCH` request to the endpoint `/api/control` containing a json body with the desired state.
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
