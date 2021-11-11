# Simultaneous AP and Managed Mode Wifi on Raspberry Pi Zero W
###### This repo was forked from https://github.com/lukicdarkoo/rpi-wifi

## About
This repo was forked from https://github.com/lukicdarkoo/rpi-wifi. We will log in this fork the settings and steps that worked for a Raspberry Pi Zero W.

- I tried multiple os versions. Some had big issues, some small. But I got it to work on Raspbian Lite 2019-07-12 (buster): https://downloads.raspberrypi.org/raspbian_lite/images/raspbian_lite-2019-07-12/
- After etching buster into a sd card and setting up ssh and wpa_suppliant.conf for remote access, run `sudo apt update`, accept the prompts.
- Once this is done run, `curl https://raw.githubusercontent.com/deathg0d/rpi-wifi/master/configure | bash -s -- -a MyAP myappass -c WifiSSID wifipass` to setup AP, where replace MyAP and myappass with ssid and password of the network you want to create and replace WifiSSID wifipass with ssid and password of your existing wifi network. Note: Make sure that the length of the password you set is greater than 8 characters, otherwise this fails.
- Reboot Pi Zero W
