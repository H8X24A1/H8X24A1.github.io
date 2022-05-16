---
label: Electric Control Modules
icon: cpu
order: 1000
---
# Setup Electric Control Modules

Control modules are devices like IP relays or smart lightbulbs. For example you can use them to turn on the lights in the meeting room at start automatically.
To setup a new control module, a correctly to the internet connected control device (e.g. Shelly1) is required.

## Setup your supported IP Relay or RGB/W Module.

### Supported Vendors and Devices

+++ Shelly
 - Shelly 1
 - Shelly 4 Pro
 - Shelly Plug S
 - Shelly Bulb
 - Shelly RGBW2
+++


+++ Rutenbeck
 - Rutenbeck TCR IP 4
+++

### Setup Shelly Device

1. Connect your Shelly device to the power grid.
 - Now a new wifi network with name starting "shelly" is available.
 - Connect to this wifi network.
 - Open your browser and open IP address 196.168.33.1 (standard shelly IP address).
 - Now you can see the menu of device.
2. Secure your device with a password.
 - Click on "Internet & Security" in the menu.
 - Open the drop down menu "RESTRICT LOGIN".
 - Check the checkbox "Restrict the web interface of the Shelly device with Username and Password".
 - You can change the username "admin" if you want.
 - Enter a secure password.
 - Click "Save".
3. Enter a device name.
 - Click of "Settings" in the menu.
 - Open drop down menu "DEVICE NAME".
 - Enter a name which describes the device well with following attributes:
  - Type of device (relay, color bulb, ...).
  - Location of device.
 - Click "Save".
4. Setup wifi connection.
 - If you use the device in larger networks, you should enable AP Roaming
 - Open drop down menu "WIFI MODE - Client".
 - Enable "Connect the Shelly device to existing WIFI Network".
 - Enter the name (SSID) of the network your want to connect to
!!!
 The Shelly device must be in the same network as the HXA.io System device or a route must be defined.
!!!
 - Enter the password of the wifi network.
 - Click "Save" and disconnect from the network.
5. Now your device is configured correctly, connected to the internet and can be used as control module.
!!!
We recommend to update the firmware of your Shelly device.
!!!


### Setup Rutenbeck Device


### Create a Control Module in HXA.io Portal
