---
title: HXA.io DOCS - HXA Room Board descripton
label: HXA Room Board
icon: paste
order: 1100
---
# HXA Room Board — HXA.io Service Description

**Version:** 1.7.0  **Date:** 2025-10-20
**Provider:** NT Technologies GmbH – powered by NetTask  

---

## 1 Overview

### 1.1 Definition
**HXA Room Board** is a visual dashboard application within the **HXA.io Ecosystem**, designed to display live booking and availability information for **Rooms, Workplaces, Workspaces, Parking Spaces, and other resources**.  
It visualizes occupancy and availability data in either a **scrollable list** or an **interactive map view**, providing real-time transparency for office and building environments.

The Room Board connects seamlessly to **Microsoft 365 Graph** and **Exchange Web Services (EWS)** through official **HXA.io Connectors**, supporting **hybrid configurations** that unify data from both cloud and on-premises systems.  
This makes HXA Room Board the ideal solution for **modern workplaces**, **smart offices**, and **digital reception or floor displays**.

### 1.2 Scope of Supply
The vendor provides the **HXA Room Board** as a **Progressive Web App (PWA)** for installation and use on supported devices and browsers.  
The service requires connection to an **HXA.io Tenant** and uses existing **Microsoft 365** or **Exchange** infrastructure for data synchronization.  
The optional **Advertising Feature** is available as a **licensed Add-on Module** and not included in the standard Room Board package.

---

## 2 Service Components

### 2.1 HXA.io Service (Backend & Portal)

#### Main Functions
- **Connector Management** – Integration of Microsoft Graph and Exchange EWS sources.  
- **Resource Management** – Selection and configuration of rooms, desks, and workspaces for display.  
- **Device Configuration** – Assignment of Room Board instances to devices via HXA.io Portal.  
- **Branding & Media** – Management of background images, logos, and advertising content (Add-on).  
- **Monitoring** – Logging of synchronization and connector health status.  

#### Supported Connectors
- **Exchange Online (Microsoft 365)** via **Microsoft Graph**  
  - *Application Connector* (App-only) – Organization-wide access.  
  - *Service Connector* (Delegated) – Access via a service account.  
- **Exchange On-Premises (2013 and later)** via **EWS**.  
- Hybrid Exchange environments are supported.

---

### 2.2 HXA Room Board App

#### Availability
- **Progressive Web App (PWA)** – runs on Chromium-based browsers (Chrome, Edge, Safari).  
- Compatible with **HXA Display**, **iPad**, **Android tablets**, **Windows devices**, and **smart info screens**.  
- Full-screen and kiosk operation supported for continuous display use.

#### Functional Highlights
- Displays live availability for rooms, desks, or parking spaces.  
- Switchable between **List View** and **Map View**.  
- Supports **hybrid data aggregation** from Microsoft Graph and EWS.  
- **Weather integration** based on building location.  
- **Advertising and informational content rotation** *(Add-on Feature)*:  
  - Supports display of **images**, **YouTube videos**, and **web content**.  
  - Administrators can define **display duration per content item** (e.g., 10–60 seconds).  
  - Enables **corporate communication**, **branding**, and **visitor information** directly on the Room Board.  
  - Requires an **active Add-on license** to activate.  
- **Smart pagination** for long resource lists.  
- **Auto-refresh** and **offline caching** capabilities.

#### Exchange Integration
Calendar and booking data are retrieved via the configured connectors using Microsoft Graph (Exchange Online) or EWS (Exchange On-Premises).

---

## 3 Customer Responsibilities & System Requirements

### 3.1 Microsoft Environment
- **Exchange Online (M365):** Setup of either an Application Connector (App-only) or a Service Connector (Delegated).  
- **Exchange On-Premises (≥ 2013):** Accessible EWS endpoint (HTTPS) and a service account with `FullAccess` to room mailboxes.  
- **Resource Mailboxes:** Created and configured with appropriate booking policies and visibility settings.  

### 3.2 Network
- Outbound HTTPS (443) access must be allowed to:  
  - `portal.hxa.io`  
  - `graph.microsoft.com`  
  - `login.microsoftonline.com`  
  - and any configured Exchange/EWS endpoints.

### 3.3 Devices
- Supported clients: **HXA Display**, **iPad**, **Android tablets**, **Windows devices**, and **info screens**.  
- Devices require registration through the **HXA.io Portal** (navigate to *Resource → Add Device → Enter Registration Code*).

---

## 4 Provisioning & Operation

### 4.1 Initial Setup
1. Create or authorize a Connector (Application or Service).  
2. Retrieve and select the desired resources from Microsoft 365 or Exchange.  
3. Configure display mode (**List** or **Map View**) and optional Add-on modules.  
4. Register the **HXA Room Board Application** in the **HXA.io Portal**.  
5. Assign configuration and publish.  

### 4.2 Maintenance
- Connector and synchronization health are monitored via portal event logs.  
- Automatic updates for the PWA are delivered through the HXA.io update service.  
- Weather and Add-on content are refreshed automatically per configuration interval.  

---

## 5 Security & Microsoft Graph Permissions

### 5.1 Application Connector (App-only)

| Permission | Type | Description |
|-------------|------|-------------|
| Calendars.Read | Application | Read calendars for all mailboxes. |
| Calendars.ReadBasic.All | Application | Read basic calendar data (free/busy). |
| Calendars.ReadWrite | Application | Create, update, and delete calendar events. |
| Directory.Read.All | Application | Read directory objects (users/groups). |
| Directory.ReadWrite.All | Application (opt.) | Modify directory objects (rarely required). |
| Place.Read.All | Application | Read room and place information. |
| Schedule.Read.All | Application | Read organization-wide schedule availability. |
| Schedule.ReadWrite.All | Application (opt.) | Modify schedules if required. |
| User.Read.All | Application | Read all user profiles. |

**Best Practices**  
- Restrict application scope using *Application Access Policies*.  
- Prefer `Calendars.ReadBasic.All` for reduced data exposure.  
- Document admin consent and limit optional permissions.

---

### 5.2 Service Connector (Delegated)

| Permission | Type | Description |
|-------------|------|-------------|
| Calendars.ReadWrite.Shared | Delegated | Read/write delegated or shared calendars (room mailboxes). |
| MailboxSettings.Read | Delegated | Read mailbox settings (working hours, timezone). |
| offline_access | Delegated | Obtain refresh tokens for persistent sessions. |
| openid | Delegated | OpenID Connect authentication. |
| Place.Read.All | Delegated | Read room and place metadata. |
| profile | Delegated | Retrieve user profile claims (OIDC). |
| User.Read | Delegated | Sign in and read user profile (service context). |
| User.ReadBasic.All | Delegated | Read basic profiles of all users (for name resolution). |

**Notes & Best Practices**  
- The service account must have `FullAccess` to relevant room mailboxes.  
- Follow least-privilege principle for all delegated access.  
- The `offline_access` grant allows continuous operation for unattended displays.

---

## 6 Support and Lifecycle
Support, maintenance, and update services follow **NT Technologies GmbH’s standard SLA** and lifecycle management policies.  
All cloud services are provided under defined availability and maintenance windows.  
Add-on features such as **Advertising & Media Rotation** are maintained under their respective **Add-on license terms**.

---

## 7 Legal Notes
“Microsoft”, “Exchange”, “Microsoft 365”, and “Graph” are trademarks of Microsoft Corporation.  
HXA.io and HXA Room Board are products of **NT Technologies GmbH / NetTask GmbH**, Germany.

---

## Appendix A – Device Registration Process

1. Install or open the **HXA Room Board** Progressive Web App.  
2. On first launch, tap **Register Device** to display a registration code.  
3. Open the **HXA.io Portal** → select the corresponding resource → **Add Device** → enter the code.  
4. Confirm and verify the synchronization status in the Portal.

---

## Appendix B – Add-on License Activation Process

1. Open the **HXA.io Portal** and navigate to **License Center**.  
2. Select **Add-on Licenses** and choose **Advertising & Media Rotation**.  
3. Assign the Add-on license to the tenant or specific Room Board application.  
4. In the **Room Board configuration**, enable the **Advertising module** under *Display Settings → Content Rotation*.  
5. Upload media files (images, videos) or enter web URLs to be displayed.  
6. Define the **rotation duration per item** and publish changes.  
7. The feature activates instantly after license validation and propagates to registered devices within minutes.

---

*© 2025 NT Technologies GmbH – All rights reserved.*