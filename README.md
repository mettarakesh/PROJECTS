
#include <ESP8266WiFi.h> 
#include <WiFiClientSecure.h> 
#include <UniversalTelegramBot.h> 
// Wi-Fi credentials 
const char* ssid = "SSID"; // Your Wi-Fi SSID  
const char* password = "PASSWORD";   // Your Wi-Fi Password 
// Telegram Bot Token 
#define BOT_TOKEN "6786802086:AAG4mJ78loSqkmIDGBB1Y3UVRK1vmDpaXIE" 
WiFiClientSecure client; 
UniversalTelegramBot bot(BOT_TOKEN, client); 
 
void setup() { 
   Serial.begin(115200); 
   WiFi.begin(ssid, password); 
 
   Serial.print("Connecting to WiFi..."); 
   while (WiFi.status() != WL_CONNECTED) { 
     delay(500); 
     Serial.print("."); 
   } 
   Serial.println("\nConnected to WiFi!"); 
 
   client.setInsecure();  // Allow SSL connection 
 
Serial.println("Waiting for a message from Telegram..."); 
 
   // Wait for incoming messages 
   while (true) { 
     int messageCount = bot.getUpdates(bot.last_message_received + 1); 
     if (messageCount > 0) { 
      Serial.println("Message received!"); 
      String chat_id = bot.messages[0].chat_id; 
      Serial.print("Your Chat ID: "); 
      Serial.println(chat_id); 
      break; 
     } 
     delay(1000); 
   } 
} 
 
void loop() { 
} 
