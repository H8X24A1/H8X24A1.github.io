---
label: Initial Setup
icon: boot-play
order: 100
---

# Microsoft 365 Resources Connector: Initial Setup

Use **Microsoft Office 365 Resources** to connect Microsoft 365 room and equipment mailboxes to HXA Room Booking and HXA Room Board. The portal describes this connector as using Microsoft Graph.

## Prepare the setup

- Identify the Microsoft 365 tenant and resource mailboxes to connect.
- Prepare an account authorized for the intended connection and any required Microsoft consent.
- Review the application-account and user/service-account approaches in [Connector Setup](/setup/connector-setup/connector-setup.md#microsoft-exchange-online-office-365).
- Prepare the [resource mailboxes](/setup/microsoft-setup/create_room-mailbox.md) to use with your HXA resources.

## Open the connector setup

1. Sign in to the [HXA.io Portal](https://portal.hxa.io).
2. Open **Connectors** in the main navigation.
3. Choose **Create connector**.
4. Locate **Microsoft Office 365 Resources** and use its **Connect** action to continue the setup.

## Choose the account type

The next panel is titled **Microsoft Office 365 Resources** and provides two options:

| Option | Connection approach |
| --- | --- |
| Application Account | Application access to the Microsoft 365 tenant |
| User/Service Account | Access in the context of the account used to connect |

Select the intended option, then use the **Connect** button on this panel to continue with authentication. The **Back** control returns to the connector selection without submitting a connection.

The **Connect** button on the connector tile and the **Connect** button on the account-type panel are separate steps. Complete the Microsoft authentication and authorization requested for the selected approach. Review the permissions presented by Microsoft before approving the request.

## Review the connection and assign resources

After completing setup, return to **Connectors** and locate the entry. Review **Type**, **Application**, **Registered from**, and **Status**. The application should match the Room Booking / Room Board use case.

In the resource configuration, review the assigned connector and calendar. See [Room Booking Resource Setup](/setup/resource-setup/room-booking-setup/resource-setup.md) or [Room Board Setup](/setup/resource-setup/room-board-setup.md).

If the connection fails, use the connector's ID to find related entries under [Settings > Event log](/maintenance/event-logs.md).

<!-- Sources: portal inspection, 2026-11-20, P03 and P15. The tile's Connect action and the account-type panel were inspected after explicit user authorization. No account type was selected and the panel's Connect button was not submitted. Microsoft sign-in, consent, exact scopes, and successful end-to-end setup remain unverified. -->
