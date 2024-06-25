---
label: Triggers
icon: cpu
order: 700
---
# Setup Triggers

Triggers are events that result in specific action. You can define these actions yourself. 
!!!
The prerequisite for setting up a new trigger is **at least one control module that has been set up**.
!!!
-  1. Login to HXA.io Portal
   -  https://portal.hxa.io. 
   - Navigate to "Automation" -> "Triggers"
-  2. Click on "Add Trigger".
-  3. Set a name for the trigger
-  4. Choose a control module and an event
-  5. Depending of what type of device you choose as control device there must to set some values:
- [x] For RGB/W controllers: the values for the colors (0-255) and an effect (optional)
- [x] For relays: port name, port at the relay, port status (on or off if event was triggered)
- [x] For Bulbs: the values for the colors (0-255) and an effect (optional)
- [x] Color example: Red: 255,0,0,0; Green: 0,255,0,0
-  6. Click on "Add".
-  7. Repeat that steps for every actions you want to use.
-  8. Scroll to the end of the page and click "Save".
-  9. At least link a resource to the trigger.
- [x] Click the three points behind the new added trigger and choose "Edit trigger".
- [x] Fill out the network configuration:
   - Port name.
   - Port number.
   - Port status.
   - Automatic switching time (ON/OFF).