---
label: Electric Control Modules
icon: cpu
order: 1000
---
# Setup Electric Control Modules

Control modules are devices like IP relays or smart lightbulbs. For example you can use them to turn on the lights in the meeting room at start automatically.
To setup a new control module, a correctly to the internet connected control device (e.g. Shelly1) is required.

## Supported Vendors and Devices

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

## Setup Shelly Device

### 1. Connect your Shelly device to the power grid.
 - Now a new wifi network with name starting "shelly" is available.
 - Connect to this wifi network.
 - Open your browser and open IP address 196.168.33.1 (standard Shelly IP address).
 - Now you can see the menu of the device.
### 2. Secure your device with a password
 - Click on "Internet & Security" in the menu.
 - Open the drop down menu "RESTRICT LOGIN".
 - Check the checkbox "Restrict the web interface of the Shelly device with Username and Password".
 - You can change the username "admin" if you want.
 - Enter a secure password.
 - Click "Save".
### 3. Enter a device name
 - Click on "Settings" in the menu.
 - Open the drop down menu "DEVICE NAME".
 !!!
 Enter a device name which describes the device well with following attributes:
 - Type of device (relay, color bulb, ...).
 - Location of device.
 !!!
 - Click "Save".
### 4. Setup wifi connection
 !!!
 In larger networks, you should "Enable AP Roaming".
 !!!
 - Open drop down menu "WIFI MODE - Client".
 - Enable "Connect the Shelly device to existing WIFI Network".
 - Enter the name (SSID) of the network your want to connect to
!!!
 The Shelly device must be in the same network as the HXA.io System device or a route must be defined.
!!!
 - Enter the password of the wifi network.
 - Click "Save" and disconnect from the network.
### 5. Now your device is configured correctly, connected to the internet and can be used as control module.
!!!
We recommend to update the firmware of your Shelly device.
!!!


## Setup Rutenbeck Device


## Create a Control Module in HXA.io Portal

### 1. Login to HXA.io Portal.
- https://portal.hxa.io
- Navigate to "Automation" -> "Control Module".
### 2. Click the green button "Add control module" and choose between:
- Relay
- RGB/W (a controller for RGBW LED stripes)
- Bulb (a controllable LED lightbulb)
### 3. Setup device
- Set a device name.
- Enter the IP address of your device.
- Enter the location of your device (optional).
- Choose device type (Shelly1, Shelly4Pro or Rutenbeck TCR IP 4).
### 4. Click Save