---
title: Local Exchange Connection via EWS - HXA Room Booking - HXA.io DOCS
label: Local EWS Connection
description: Connect HXA Room Booking on an HXA Display directly to an on-premises Exchange Server over the local network, without routing calendar data through HXA.io Services.
icon: shield
order: 90
---

# HXA Room Booking: Local Exchange Connection via EWS

The optional local Exchange connection add-on allows the HXA Room Booking software on an HXA Display to communicate directly with an on-premises Microsoft Exchange Server. The display accesses the room calendar through Exchange Web Services (EWS) over the customer's local network.

**In this connection mode, calendar data is exchanged directly between the HXA Display and the local Exchange Server. It is not routed through HXA.io Services.**

This option is intended for organizations with heightened requirements for protecting confidential calendar information, including law firms, tax advisory firms, government agencies, and military organizations.

<!-- Editorial follow-up requested by the product owner on 2026-11-20:
TODO: Document the minimum HXA Room Booking software version required for the local EWS connection add-on once confirmed. Do not infer it from the version in the product description.
TODO: Add the detailed activation and on-display configuration steps, including the actual menu labels, required fields, and screenshots, once confirmed. The configuration overview below is not the final step-by-step guide.
-->

## Connection Model and Data Flow

The HXA Room Booking software on the display connects to the local Exchange Server's EWS interface. The credentials required for this connection are configured directly on each HXA Display.

HXA.io Services remain involved in function settings, configuration, and licensing.

| Communication | Connection path |
| --- | --- |
| Calendar data for the connected room calendar | Directly between the HXA Display and the local Exchange Server via EWS |
| Function settings and configuration | Between the HXA Display and HXA.io Services |
| Licensing | Between the HXA Display and HXA.io Services |

!!! info HXA.io connectivity is still required
The local Exchange connection does not provide fully offline operation. Connectivity to HXA.io Services is still required for function settings, configuration, and licensing.
!!!

## Requirements

- HXA Room Booking software running on an HXA Display.
- A purchased and activated local Exchange connection add-on.
- An on-premises Microsoft Exchange Server 2016, 2019, or Subscription Edition (SE).
- A configured room mailbox and calendar.
- An EWS endpoint reachable from the HXA Display over the local network.
- Credentials with the permissions required to access the room calendar.
- Connectivity to HXA.io Services for function settings, configuration, and licensing.

!!! warning Exchange Server lifecycle
Technical compatibility with HXA Room Booking is separate from Microsoft's product support lifecycle. Microsoft support for Exchange Server 2016 and 2019 ended on October 14, 2025. Take the server's support status into account when planning and operating this connection.
!!!

See [Microsoft's Exchange Server 2016 and 2019 end-of-support guidance](https://learn.microsoft.com/en-us/troubleshoot/exchange/administration/exchange-2019-2016-end-of-support).

## Activation and Configuration Overview

Purchase and activate the local Exchange connection add-on. Prepare the room calendar and the EWS access credentials, and ensure that the display can reach the local Exchange Server.

Configure the connection details and the credentials required for EWS access directly on each HXA Display. Keep the display's connection to HXA.io Services available for function settings, configuration, and licensing.

After configuration, use an existing or newly created test appointment to check that the room calendar is displayed correctly.

## Frequently Asked Questions

### Is calendar data sent through HXA.io Services?

When the local EWS connection is activated and configured, calendar data for the connected room calendar is exchanged directly between the HXA Display and the local Exchange Server. It is not routed through HXA.io Services.

### Can I completely block the connection to HXA.io Services?

This connection mode still requires communication with HXA.io Services for function settings, configuration, and licensing.

### Where do I configure the Exchange credentials?

Configure the credentials required for EWS access directly on each HXA Display.

### Does this connection mode apply to Exchange Online?

This article describes direct EWS access to an on-premises Exchange Server over the local network. For Exchange Online, see the [Microsoft 365 connector setup](/setup/connector-setup/microsoft-365/initial-setup.md).

## Related Documentation

- [HXA Display setup](/setup/device-setup/room-booking/hxa-system.md)
- [HXA Room Booking product description](/appendix/product-descriptions/app-description-roombooking.md)
