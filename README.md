
## WiFiManager
<https://github.com/tzapu/WiFiManager>

ESP8266 WiFi Connection manager with fallback web configuration portal

The configuration portal is of the captive variety, so on various devices it will present the configuration dialogue as soon as you connect to the created access point.

**How It Works:**

- when your ESP starts up, it sets it up in Station mode and tries to connect to a previously saved Access Point
- if this is unsuccessful (or no previous network saved) it moves the ESP into Access Point mode and spins up a DNS and WebServer (default ip 192.168.4.1)
- using any wifi enabled device with a browser (computer, phone, tablet) connect to the **newly created Access Point(ESPxxxxx)**
- because of the Captive Portal and the DNS server you will either get a 'Join to network' type of popup or get any domain you try to access redirected to the configuration portal
- choose one of the access points scanned, enter password, click save
- ESP will try to connect. If successful, it relinquishes control back to your app. If not, reconnect to AP and reconfigure.


