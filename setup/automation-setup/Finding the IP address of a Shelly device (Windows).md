---
label: Finding the IP address of a Shelly device (Windows)
icon: cpu
order: 900
---
# Finding the IP address of a Shelly device (Windows)

+++ Folow these steps

To find out the IP address of a device you need the "Advanced IP Scanner".
Here you find the download:
[!ref target="blank" text="Advanced IP Scanner"](https://www.advanced-ip-scanner.com/)

- Once downloaded, open the program, select your language and click OK.
- The following menu should pop up.

![](/images/advanced_ip_scanner-setup.png)

- Select Run and then click Run.
- Now make sure you are connected to the network the device is located.
- Then click “Scan” on the top left.
- After a while, you should see several IP addresses in the list.
- Now look for IP addresses where the Manufacturer column is empty.
- Right-click on each of the addresses, select "Tools" and then "HTTP".

![](/images/advanced_ip_scanner-http.png)

- If a Shelly menu page loads, you have found a Shelly device.

![Here is an example of a Shelly Color Bulb menu page.](/images/advanced_ip_scanner-shelly_page.png)

- You can now find the right device using the previously defined name (see top center) if there are several devices in the network.
- The address of the menu page is the IP address of the device.

+++