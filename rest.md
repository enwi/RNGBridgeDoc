# REST API
Currently you can control only the load output via the rest interface.
For that you have to send a `POST`, `PUT` or `PATCH` request to the endpoint `/api/control` containing a json body with the desired state.
To turn the load output on the body needs to contain `{"enabled":true}`, to turn it off `{"enabled":false}`.

You can also try this using `curl` for that replace the placeholer `IP` with the ip address of `RNGBridge`:
```shell
curl -X POST -H "Content-Type: application/json" -d '{"enabled":true}' IP/api/control
```

> Note if you have setup automatic control of the load output you might be able to change the state of the output using the REST interface, but it will probably be overwritten by the automatic control.
> So make sure that automatic control is disabled if you want to use this feature.
