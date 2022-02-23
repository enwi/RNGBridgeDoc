# PVOutput
`RNG to WiFi` can publish the data read from your Charge Controller to PVOutput, thus making it accessible outside your local network as well as providing in depth charts and analytics of your system throughout the year.

## Setup
1. If you do not have a PVOutput account yet, create one [here](https://pvoutput.org)
2. If you do not have a PVOutput system setup yet, create one [here](https://pvoutput.org/addoutput.jsp)
3. Go to your account settings [here](https://pvoutput.org/account.jsp) and scroll down until you see `API Settings`
4. Set `API Access` to `Enabled`
5. If you do not see an `API Key` press the `New Key` button once
6. Open the `RNG to WiFi` user interface and open the `PVOutput` tab ([shortcut](http://rngbridge.local/#tab2))
7. Copy the `API Key` from pvoutput.org and paste it into the `API Key` field of `RNG to WiFi`
8. On pvoutput.org scroll down to `Registered Systems` and copy the `System Id` of the system you want to uplaod the data for and paste it into the `System ID` field of `RNG to WiFi`
9. Depending on your Region enter the time offset from UTC of your local time zone in the `Time offset from UTC` field. (For Germany this is +2)
10. Enable the PVOutput service by enabling the `Enable` switch
11. Watch the `Status` field, it should briefly display `Starting` and then `Running` if everything went according to plan. After 5 to 15 minutes (depending on your PVOutput `Status Interval` setting) it should display `Sent power data` and data should be available on pvoutput.org

## Troubleshooting