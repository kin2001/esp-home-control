# ESP8266 Home Control with Captive Portal + Internet Access

This project allows you to control a **light** and **fan** using an ESP8266 via:

- 📶 Captive Portal (for setup)
- 🌐 Full Internet Access (via port forwarding)

## ✨ Features

- Simple control interface (light/fan toggle)
- Wi-Fi setup via captive portal
- EEPROM saves credentials and device state
- Optional HTTP basic authentication
- Online control from anywhere using DDNS or public IP

## 🛠 Hardware Used

- ESP8266 (NodeMCU, Wemos D1 Mini, etc.)
- Relay modules
- Fan/light connected to relays

## 🚀 Getting Started

1. Flash the code to your ESP8266
2. On first boot, connect to `HomeWifiControl` AP and go to any page (captive portal)
3. Enter your Wi-Fi SSID/password
4. Reboot into **online mode**
5. [Configure your router for port forwarding](#internet-access)

## 🌐 Internet Access

To control the ESP8266 from the internet:

1. Set up **port forwarding** on your router
2. (Optional) Use **Dynamic DNS** like [No-IP](https://www.noip.com/)
3. Access your ESP at `http://your-public-ip:PORT` or DDNS domain

> ⚠️ Add authentication if exposing to the internet

## 🔐 Optional: Basic Auth

Uncomment and set these in `main.ino` to protect access:

```cpp
const char* http_username = "admin";
const char* http_password = "home123";
