# Microsoft Exchange Connector: Initial Setup

This page covers starting a **portal-based Microsoft Exchange connector**. The portal's connector selection describes this connection as using Exchange Web Services (EWS).

## Prepare the setup

- Identify the Exchange environment and room calendars you intend to connect.
- Prepare the EWS endpoint and an account with access to those calendars.
- Check endpoint reachability and the applicable [firewall configuration](/setup/firewall-setup.md).
- Prepare the [room mailboxes](/setup/microsoft-setup/create_room-mailbox.md).

## Open the connector setup

1. Sign in to the [HXA.io Portal](https://portal.hxa.io).
2. Open **Connectors > Create connector**.
3. Locate **Microsoft Exchange** and use its **Connect** action to continue with the connection settings.

## Connection form

The **Microsoft Exchange** panel contains:

| Field or control | Purpose |
| --- | --- |
| Mailbox Address | Address of the Exchange account used for the connection |
| Password | Password for that account |
| Connect | Submit the connection details |
| Back | Return to connector selection without submitting the form |

The initial form does not show a separate EWS service-URL field. This view alone does not establish how the endpoint is determined or which additional settings may follow submission.

The selection page also contains **Microsoft Exchange Sparo**, the separate product-specific option for Sparo. Its initial panel has the same **Mailbox Address**, **Password**, **Connect**, and **Back** controls.

Enter the connection account's details when performing the actual setup, then continue with **Connect**. A displayed form is not confirmation that authentication or calendar access has succeeded.

## Review the connection

After completing the connector's setup, locate it in the overview and check **Type**, **Application**, **Registered from**, **Status**, and **Service URL**. Use its **Connector ID** to find related errors in [Event Logs](/maintenance/event-logs.md).

Assign the connector and intended calendar to the appropriate resource; see [Room Booking Resource Setup](/setup/resource-setup/room-booking-setup/resource-setup.md).

## Direct display-to-Exchange connection

For the optional direct connection between an HXA Display and an on-premises Exchange Server over the local network, see [Local Exchange Connection via EWS](/setup/connector-setup/microsoft-exchange/local-ews-connection.md).
