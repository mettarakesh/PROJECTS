Sending Data from ESP8266 to Telegram 
Sending data from **ESP8266 to Telegram** involves connecting the ESP8266 to WiFi, 
reading sensor data, and using the **Telegram Bot API** to send messages via HTTPS 
requests. The ESP8266 formats the data into a URL and sends it using `WiFiClientSecure` 
and `HTTPClient`. 🚀 
Steps to create an BoT in Telegram:- 
 Open Telegram App. 
 Search for BotFather. 
 Type /newbot and press Enter. 
 Enter a bot name (e.g., "ESP8266_Bot"). 
 Choose a username (must end with "bot", e.g., "ESP8266SensorBot"). 
 Copy the Bot Token (you’ll need it later). 
✅ Example Token: 123456789:ABCDEF123456789abcdef123456789abc 
Steps to get an Chat ID:- 
 Enter the following code in the arduino ide to get an chat ID. 
 Upload this code to ESP8266. 
 Open Serial Monitor (Baud Rate: 115200). 
 Send any message to your bot on Telegram. 
 Wait a few seconds → Your Chat ID will appear in the Serial Monitor.
