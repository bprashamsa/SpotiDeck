# SpotiDeck
A pocket-sized Spotify controller built on a touchscreen ESP32 board! Meaning you can play, pause, skip, and see what's playing without ever opening a browser tab

# Features:
- Play / Pause Skip forward / back
- Live "Now Playing" display — track name, artist, album
- Custom touchscreen UI, hand-drawn/designed graphics
-  Talks directly to the Spotify Web API over Wi-Fi, no separate relay server needed!

# Hardware 
- Board: Hosyond 3.5" ESP32 Display — ESP32-WROOM-32, dual-core, 240MHz
- Display: 3.5" 320x480 TFT, ST7796U driver
- Touch: Resistive touchscreen
- Connectivity: Wi-Fi (2.4GHz)
- Power: USB-C

# How It Works: 
SpotiDeck runs entirely on the ESP32!
It talks to the Spotify Web API directly over HTTPS: 
On first boot (or via a one-time setup step on your computer), you authorize the device with your Spotify account and obtain a refresh token. 
That refresh token is stored on the device. The firmware uses the refresh token to request short-lived access tokens as needed, then calls Spotify's endpoints. 
Track info and album art are pulled down and rendered on the display; touch input on the screen triggers the corresponding API calls. 

** PSA: You'll need a Spotify Premium account, playback control endpoints require Premium. ***
