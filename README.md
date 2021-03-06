# ESP32S2 Camera + Websockets stream

ESP32S2 with OV2640 Camera websockets stream example. JPEG images captured from camera is streamed to server via websockets. User can view the stream at browser. Current implementation can achieve around 15 fps.

Another version using udp is available [here](https://github.com/wms2537/esp32s2-camera-udp).

Code is written with esp-idf.

## Backend
The backend is based on my [Python MJPEG Websockets Server](https://github.com/wms2537/python-websockets-mjpeg-server).

## Getting Started
### Hardware
This schematic contains an e-paper module used [here](https://github.com/wms2537/esp32s2-epaper-qr). You can ignore it. 

![Schematic](/images/Schematic_ESP32S2CAM.png)

I designed a pcb for it.

![PCB](images/pcb.jpeg)

### Code
Change these lines in `main/esp32s2_camera.c`
```c++
#define EXAMPLE_ESP_WIFI_SSID "YOUR_WIFI_SSID"
#define EXAMPLE_ESP_WIFI_PASS "YOUR_WIFI_PASSWORD"
#define WEBSOCKETS_BACKEND_URL "YOUR_WEBSOCKETS_SERVER_URL"
```

Start backend server and view stream from browser `http://localhost:3000`