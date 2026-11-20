# Device Monitoring

Open **Devices** in the [HXA.io Portal](https://portal.hxa.io) for **Devices | Overview**. Use **Search**, **Filter**, and **Columns option** to locate a device.

| Column | Information |
| --- | --- |
| Name | Device name |
| Serial No. | Serial identifier |
| Device ID | Portal identifier |
| Register date | Registration timestamp |
| Status | Device status indicator |
| App-Version | Reported application version |
| Platform | Client platform |
| Last online | Last-online timestamp shown by the portal |

## Check a resource's devices

1. Open **Resources > Options > Edit Resource**.
2. Find **Application/ Devices**.
3. Match the device by Device ID or serial identifier.
4. Review its Online indicator, App-Version, Platform, and Last online.

Room Booking labels its device table **Interactive Displays**. Registration is described in the corresponding [Room Booking](/setup/resource-setup/room-booking-setup/resource-setup.md) or [Room Board](/setup/resource-setup/room-board-setup.md) setup article.

## Investigate missing updates

Check the resource assignment and any feature-specific app-version notices. Compare the last-online time with the issue, then check network access and the application on the device.

For calendar or connector issues, inspect the assigned connector and [Event Logs](/maintenance/event-logs.md). Include the device ID, app version, platform, and displayed timestamps in a support request.
