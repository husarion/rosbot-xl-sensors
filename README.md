# rosbot-xl-sensors
Visualization for ROSbot XL sensors.

## Quick start

**1. Connect to your ROSbot via ssh.**

```bash title="user@device:~$"
ssh husarion@<ROSBOT_IP/HUSARNET_NAME>
```

**2. Clone the repository on your ROSbot.**

```bash title="husarion@husarion:~$"
git clone https://github.com/husarion/rosbot-xl-sensors
cd rosbot-xl-sensors
```

**3. Run Docker Compose.**

```bash title="husarion@husarion:~/rosbot-xl-sensors$"
docker compose up
```

**4. Open Foxglove application in browser.**

To open Foxglove type `<ROSBOT_IP/HUSARNET_NAME>:8080` in your browser search bar. 

:::info
You should use **Chrome/Chromium** browser.
:::

**5. Open connection.**
 
Inside Foxglove application, find **Data source** on left top and click the **`+`** then click `Open connection`. Use default **WebSocket URL** `ws://<ROSBOT_IP/HUSARNET_NAME>:9090` and click `Open`.

### Result

<div style={{width: '85%', margin: 'auto'}}>

![](/img/other/foxglove_xl_result.gif)

</div>

![foxglove_result](.docs/foxglove_xl_result.gif)
