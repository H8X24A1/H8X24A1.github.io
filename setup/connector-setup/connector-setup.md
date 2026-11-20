---
label: Connector Setup
icon: repo-forked
order: 900
---

## Find connectors

Open **Connectors** in the main navigation of the [HXA.io Portal](https://portal.hxa.io). Use **Create connector** to open the connector selection page.

| Portal selection | Purpose | Documentation |
| --- | --- | --- |
| HXA.io Local Connector | HXA-hosted calendars; the portal describes this connector as automatically created for the organization | [Calendar Setup](/setup/calendar-setup.md) |
| Microsoft Exchange | Exchange connection using EWS | [Exchange Setup](/setup/connector-setup/microsoft-exchange/initial-setup.md) |
| Microsoft Exchange Sparo | Exchange integration for Sparo | [Exchange connection form](/setup/connector-setup/microsoft-exchange/initial-setup.md#connection-form) |
| Microsoft Office 365 Resources | Microsoft Graph access to room and equipment mailboxes for Room Booking and Room Board | [Microsoft 365 Setup](/setup/connector-setup/microsoft-365/initial-setup.md) |
| Microsoft Entra ID (Microsoft 365 Azure Active Directory) | Directory integration for Sparo; also required by the floor-plan links editor | [Entra ID Setup](/setup/connector-setup/microsoft-entra-id/initial-setup.md) |
| Office 365 - Teams | Teams integration | [Teams Setup](/setup/connector-setup/microsoft-teams/initial-setup.md) |

The HXA.io Local Connector is a calendar-host option in the portal. For a display that connects directly to an on-premises Exchange server, see [Local Exchange Connection via EWS](/setup/connector-setup/microsoft-exchange/local-ews-connection.md).

## Check an existing connector

The overview provides Search, Filter, and Columns option. Available columns include **Connector ID**, **Type**, **Application**, **Registered from**, **Status**, **Created**, and **Service URL**. Active entries show **Active** in the status indicator.

Match the connector's application to the resource you are configuring. For troubleshooting, use its Connector ID to locate related entries under **Settings > Event log**; see [Event Logs](/maintenance/event-logs.md).

## What the first Connect action opens

The **Connect** action on each product tile opens its initial configuration panel:

| Connector | Initial selection or fields |
| --- | --- |
| Microsoft Office 365 Resources | Application Account or User/Service Account |
| Microsoft Exchange / Microsoft Exchange Sparo | Mailbox Address and Password |
| Microsoft Entra ID | Application Account |
| Office 365 - Teams | User/Service Account or Teams Calling Agent (User/Service Account) |

Each panel has its own **Connect** button for continuing or submitting the setup, plus **Back** to return to the tile selection. Opening a panel and completing authorization are separate steps.

<!-- Current selection, overview, and initial panels verified in the portal on 2026-11-20, P03/P15–P18. Sign-in, consent, and connection submission were not executed. -->

## Microsoft Exchange Online (Office 365)
There are two types of connectors to connect to Microsoft Exchange Online (Office 365):
- via Microsoft Office 365 Application account or
- via Microsoft Office 365 User/Service account

### Setup via Microsoft Office 365 Application account

An application connector uses application access to the Microsoft 365 tenant. The Microsoft consent request determines the permissions being granted; it does not imply access to all information in the tenant.

- To do this, log in to the HXA.io portal at https://portal.hxa.io.
- Open **Connectors > Create connector**.
- Open **Microsoft Office 365 Resources > Connect**.
- Select **Application Account**, then use the panel's **Connect** button to continue with Microsoft authentication.

!!!
Use an administrator authorized to grant the requested Microsoft permissions. Review the consent request for the selected connector.
!!!

### Setup via Microsoft Office 365 Service account

A user/service connector operates in the context of the account used to connect it. Prepare access to the room calendars this account is intended to manage. The exact permissions depend on the connector's authentication and access model.

Use a Microsoft 365 user/service account if you want to authorize a single connector to access custom and shared calendars.

- To do this, log in to the HXA.io portal at https://portal.hxa.io.
- Open **Connectors > Create connector**.
- Open **Microsoft Office 365 Resources > Connect**.
- Select **User/Service Account**, then use the panel's **Connect** button to continue with Microsoft authentication.


## Microsoft Entra ID

This connector type is required to set up the HXA Sparo application and only supports the application account type. A prerequisite for setting up this connector is that the account must be mail-enabled, meaning the account used to configure the connector requires at least a Microsoft Exchange Online Plan 1 license.

The portal's initial panel provides **Application Account** and a separate **Connect** button. See [Microsoft Entra ID Initial Setup](/setup/connector-setup/microsoft-entra-id/initial-setup.md) for the navigation and related directory workflows.
