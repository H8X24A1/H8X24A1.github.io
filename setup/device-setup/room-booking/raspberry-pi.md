---
label: Raspberry Pi
icon: device-desktop
order: 800
---

# Deploy HXA Room Booking WebApp on Raspberry Pi via Chromium Kiosk Mode (Bash-Script)

### Note

This is still a beta version. The Script just configures the Raspberry Pi to open Chromium automatically on boot, disables mouse cursor, panel and screensaver. Additionally it changes the splash screen and wallpaper (to HXA.io 1 logo) and configures the display to run in portrait mode if wanted.

### WARNING!
!!!
Still there is no security enhancement or hardening included for the Raspberry Pi OS for running in kiosk mode!
!!!

### Download Raspberry Pi OS Image

Go to https://www.raspberrypi.org/software/operating-systems/#raspberry-pi-os-32-bit and download the version Raspberry Pi OS Desktop. (The middle-sized version - around 1200 MB)

### Flash Image to SD-Card

Go to https://www.balena.io/etcher/ and download the software balena Etcher, start the software and choose the downloaded image as source and your SD-Card as target.

### Next Steps

- Insert SD-Card into Raspberry Pi
- Connect a keyboard to the Raspberry Pi
- Start the Raspberry Pi (connect power)
- Do first configuration stuff (Press Enter through the setup - but DO NOT UPDATE! The script will perform a system update after automatically removing unnecessary software)
- Open a terminal by pressing CTRL + ALT + T

- Download the configration script package:

`wget https://script.roombooking.hxa.io/raspberry-pi/HXA-RB-RASPI-Rollout-Script.zip`

- Unzip the zip-file:

`unzip HXA-RB-RASPI-Rollout-Script.zip`

- Go to unzipped directory:

`cd HXA-RB-RASPI-Rollout-Script`

- Make script-file executable:

`chmod +x HXA-RB-RASPI-Rollout-Script.sh`

- Start the script:

`sudo ./HXA-RB-RASPI-Rollout-Script.sh`

- After performing deployment, the the script automatically removes some unnecessary software and then performing a system update. Therefore you should not perform an update while the first system configuration.

- At least Raspberry Pi will restart automatically and start into HXA Room Booking 2 App.
