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

**3. Flash firmware.**

```bash title="husarion@husarion:~$"
docker stop rosbot-xl microros || true && \
docker run --rm -it --privileged \
--mount type=bind,source=/dev/ttyUSBDB,target=/dev/ttyUSBDB \
husarion/rosbot-xl:humble-0.8.2-20230913 \
flash-firmware.py -p /dev/ttyUSBDB
```

**4. Run Docker Compose.**

```bash title="husarion@husarion:~/rosbot-xl-sensors$"
docker compose up
```

**5. Open Foxglove application in browser.**

To access Foxglove, input the following in your browser's search bar:

- `http://<localhost>:8080/ui` - if you work locally,
- `http://<ROSBOT_IP>:8080/ui` - if you want to connect to a device connected to the same LAN,
- `http://<HUSARNET_NAME>:8080/ui` - if you want to connect to the device using Husarnet VPN.

> [!NOTE]
> You should use the **Chrome/Chromium** browser and wait a few seconds after running `docker compose` to ensure all images boot up correctly.

### Result

![foxglove_result](.docs/foxglove_xl_result.gif)
