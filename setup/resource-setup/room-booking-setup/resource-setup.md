# Room Booking Resource Setup

Configure Room Booking under **Resources** in the [HXA.io Portal](https://portal.hxa.io). A resource brings together its calendar, devices, license, and application settings.

## Add a resource

To set up and link a device to a Microsoft Exchange On-Premise or Microsoft 365 resource you have to create a new resource inside the HXA Portal Resource Overview.

- Select the resource Type "Room (Room Booking)".
- Enter a room name.
- Select a license.
- Select a connector.
- Select a calendar.
- Add a device or skip for later.

## Edit a resource

To edit a resource you have to check the resources overview list for the specific resource you want to edit.

- Click in the column "options" on the three dots and click "Edit resource".
- Scroll down to the section where you want to make changes.

## Resource details and connections

| Section | Settings and information |
| --- | --- |
| General information | Display name, Category, language, location details, Building, Floor, Floorlabel, Capacity, and Window Orientation |
| Connector | Assigned connection and connector controls |
| Calendar | Calendar assigned to this resource |
| Application/ Devices | Connected Interactive Displays and their status, App-Version, Platform, and Last online information |
| Resource images | Up to three images, each no larger than 1 MB |
| Branding settings | Separate backgrounds for Available, Pending, and Busy; Christmas Mode and its date range |
| Resource QR Code | Download QR Code |
| Licensing / Licensing - Add-ons | Assigned product and add-on licenses, including expiry dates |

Calendar-supplied location and capacity fields can be read-only. Check the connected calendar's metadata when a field cannot be edited here.

The separate resource-picture upload recommends **800 × 800 pixels** and allows **jpeg**, **jpg**, and **png**. It also offers **Load mailbox profile picture** and **Load standard picture**. This resource picture is separate from the status-specific display backgrounds.

See [Background Image Setup](/setup/resource-setup/room-booking-setup/background-image-setup.md) and [Device Monitoring](/maintenance/device-monitoring.md).

## Advanced settings

The **Advanced settings** section has six tabs. Configure the intended options and use its **Save and Update** button.

### Dashboard settings

- **Select Design** and **Select colorset** configure the dashboard's appearance.
- **Enable Screen Saver**, **Select clock type**, and **Display screensaver after (Seconds)** configure the screensaver.
- **Display weather forecast** and **Add location** configure the weather display.
- **Enable floor plan** controls floor-plan availability on the display. Prepare the map separately under [Floor Plans](/setup/floor-plan-setup.md).

### Energy & Power management

This tab provides **Enable energy saving mode for HXA Devices**. Further fields can depend on the feature's state and the connected device. Review the options displayed for your configuration before saving.

### Booking & interaction

This tab contains **Enable quick booking**, **Allow attendees**, and a **Maximum duration** slider. The slider is labeled in hours. Choose the quick-booking duration limit appropriate for the resource.

### Events display options

| Field | Setting |
| --- | --- |
| Display period of planned events (days in future) | How far ahead the display lists planned events |
| Maximum planned events to be displayed (in the future) | Number of future events to display |
| Name of directly booked events on the display | Display naming for directly booked events |
| Name of scheduled events on the display | Display naming for scheduled events |

### Custom titles & event meta data

Use **Activate additional titles** and **Additional names for events** to maintain the list of selectable event titles. **Allow custom title** is a separate option. See [Quick Meeting Title Setup](/setup/resource-setup/room-booking-setup/quick-meeting-title-setup.md).

### Automation & attendance

| Setting | Related controls |
| --- | --- |
| Activate check-in / check-out for events | Enable the check-in/out feature |
| Activate early check-in to events | Show check-in Button before event starts |
| Cancel events automatically | Automatically cancel after |
| Activate only check-out for events | Separate check-out-only option |
| Activate extend event functionality | Device selection and Manage Devices |
| Checkout Authentication | Authentication option for check-out |

Review these settings together when configuring attendance handling. Select the intended devices for the extend-event feature. Verify the resulting behavior on a suitable test appointment after saving; a selected portal option alone does not confirm client behavior.

## Add-On Licenses

The add-on configuration provides tabs for **Room Service**, **Timer**, and **Room Temperature**. Available features depend on the assigned add-on licenses.

The Room Service tab includes its own device selection, order recipients, article activation, and **Save and Update**. See [Room Service Setup](/setup/room-service-setup.md).

## Check the result

Reopen the resource to check saved settings. Review device status and app versions, then verify the intended display, booking, and attendance behavior on a test resource. For connection errors, see [Event Logs](/maintenance/event-logs.md).

## Delete a resource

To delete a resource please open the resource overview page and find the resource you want to delete.

- Click on the column "options" on the tree dots and choose "Delete resource"
- Confirm the dialog if you really want to delete this resource.
