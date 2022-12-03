# PVOutput
`RNGBridge` can publish the data read from your Charge Controller to PVOutput, thus making it accessible outside your local network as well as providing in depth charts and analytics of your system throughout the year.

## Setup
1. If you do not have a PVOutput account yet, create one [here](https://pvoutput.org)
2. If you do not have a PVOutput system setup yet, create one [here](https://pvoutput.org/addoutput.jsp)
3. Go to your [account settings](https://pvoutput.org/account.jsp) and scroll down until you see `API Settings`
4. Set `API Access` to `Enabled`
5. If you do not see an `API Key` press the `New Key` button once
6. Open the `RNGBridge` user interface and go to the settings menu by clicking the gear icon in the top right of the page.
7. Click on the panel named `PVOutput`.
8. Enable `PVOutput`.
9. Copy the `API Key` from pvoutput.org and paste it into the `API Key` field of `RNGBridge`
10. On pvoutput.org scroll down to `Registered Systems` and copy the `System Id` of the system you want to uplaod the data for and paste it into the `System ID` field of `RNGBridge`
11. Depending on your Region enter the time offset from UTC of your local time zone in the `Time offset from UTC` field. (For Germany this is +2 in the summer and +1 in the winter due to daylight saving)
12. If you verified your settings press the `SAVE PVOUTPUT CONFIG` button
13. `RNGBridge` will reboot and try to fetch the update interval from pvoutput.org, sync the time and then upload your systems data every 5, 10 or 15 minutes (depending on what you set in the settings on pvoutput.org)
14. The status on the `RNGBridge` settings page should display `Starting` followed by `Syncing time` followed by `Running` repeatedly followed by `Sent data (hour:minute)` where `hour:minute` is the timestamp of when the data was sent to pvoutput.org

<img src="https://github.com/enwi/RNGBridgeDoc/blob/v2/images/gif/pvo.gif" width="600">

## Troubleshooting
### Status field shows `Could not get update interval, retrying`
- Check if both your `API Key` and `System ID` are correct and press the `SAVE PVOUTPUT CONFIG` button if you made changes
- Check if pvoutput.org is reachable
- Check if your network has a valid internet connection
- If you still have issues get help on my discord server by clicking on this icon -> [![Discord](https://img.shields.io/discord/781219798931603527.svg?label=enwi&logo=discord&logoColor=ffffff&color=7389D8&labelColor=6A7EC2)](https://discord.gg/YxVyJWX62h)

### Status field shows `Could not send power data`
- Check if pvoutput.org is reachable
- Check if your network has a valid internet connection
- If you still have issues get help on my discord server by clicking on this icon -> [![Discord](https://img.shields.io/discord/781219798931603527.svg?label=enwi&logo=discord&logoColor=ffffff&color=7389D8&labelColor=6A7EC2)](https://discord.gg/YxVyJWX62h)

### Status field shows `No WiFi for time sync`
- Check if your network has a valid internet connection
- If you still have issues get help on my discord server by clicking on this icon -> [![Discord](https://img.shields.io/discord/781219798931603527.svg?label=enwi&logo=discord&logoColor=ffffff&color=7389D8&labelColor=6A7EC2)](https://discord.gg/YxVyJWX62h)