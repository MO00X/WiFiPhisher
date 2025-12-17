# WiFiPhisher
ESP8266‑WiFiPhisher — ESP8266‑based rogue access‑point for Wi‑Fi phishing using captive portal and deauth attacks.
# ESP8266-WiFiPhisher
# 🚨 ESP8266 Evil Twin & Deauth Attack Tool

> ⚠ *Educational & Penetration Testing Tool Only*  
> This tool is intended *strictly for educational purposes* or *authorized penetration testing*. Misuse of this tool is illegal and unethical. Always obtain permission before scanning or attacking any network.

---

## 🔍 Overview

This project uses an *ESP8266* with a *128x32 OLED display* to perform advanced Wi-Fi attacks including:

- *Deauthentication attack* to disconnect users from real networks
- *Evil Twin attack* to create a fake access point (AP) identical to the original
- A *web portal* that appears when users connect to the fake AP, asking for the original network password
- Password verification and *real-time password display* on the OLED screen

> The tool acts as a Wi-Fi honeypot and password harvesting system, all in one compact ESP8266-based device.

---

## 🧠 Features

✅ Evil Twin Access Point creation  
✅ Deauth all users from target Wi-Fi  
✅ Fake login portal served over the fake AP  
✅ Password entry verification with original AP  
✅ Password display on OLED screen if correct  
✅ Dedicated AP (ESP8266PasswordCracker) for user control

---

## ⚙ Components Used

| Component           | Description                     |
|--------------------|---------------------------------|
| ESP8266            | NodeMCU or Wemos D1 Mini         |
| OLED Display       | 128x32 (SSD1306) via I2C         |
| Micro USB Cable    | Power & programming              |

---

## 🔌 Working & Workflow

1. *Power on the device*
   - AP created: ESP8266PasswordCracker
   - Password: Balwant@024161


2. *User connects to the device AP*  
   → A web portal opens with options:
   - Launch Evil Twin Attack
   - Launch Deauth Attack

3. *Evil Twin Attack Flow*:
   - Fake AP is created with same SSID as target
   - Original users are deauthed (disconnected)
   - Victim auto-connects to fake AP
   - Web portal asks for Wi-Fi password
   - If entered password is correct (checked against real AP), it's:
     - Displayed on OLED screen
     - User is connected to original AP

4. *OLED Display Shows*:
   - Attack Status
   - Captured Password (if successful)
   - Target SSID

---

## 📲 How to Use

1. Flash the ESP8266 with the provided code using Arduino IDE.
2. Install required libraries:
   - ESP8266WiFi
   - ESPAsyncWebServer
   - ESPAsyncTCP
   - Adafruit_SSD1306
   - Adafruit_GFX
3. Connect to ESP8266PasswordCracker and open the portal.
4. Launch desired attack and monitor password capture via OLED.
---

## 📷 Screenshots 

![ESP8266-WiFiPhisher Side View](https://github.com/balwantyadav1/ESP8266-WiFiPhisher/blob/main/Image/ESP8266-WiFiPhisher.jpg)

![ESP8266-WiFiPhisher Side View](https://github.com/balwantyadav1/ESP8266-WiFiPhisher/blob/main/Image/web-portal.jpg)

![ESP8266-WiFiPhisher Side View](https://github.com/balwantyadav1/ESP8266-WiFiPhisher/blob/main/Image/web-portal2.jpg)

![ESP8266-WiFiPhisher Side View](https://github.com/balwantyadav1/ESP8266-WiFiPhisher/blob/main/Image/ESP8266-WiFiPhisher-ID-Password.jpg)

---

## 🛠 TODO / Improvements

- Save passwords to EEPROM/SD card  
- Add more social engineering templates (Facebook, Instagram, etc.)  
- Display attack logs on web portal  
- Auto-email stolen credentials (for lab simulations only)

---

## ⚠ Legal Disclaimer

This software is developed for *educational purposes only*.  
Any misuse or unauthorized attack on third-party networks is *illegal* and *against the terms of use* of this project.  
The author is *not responsible* for any damage or misuse.

---
