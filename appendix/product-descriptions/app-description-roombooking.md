---
title: HXA.io DOCS - HXA Room Booking descripton
label: HXA Room Booking
icon: paste
order: 1100
---
# HXA Room Booking – Application Service & HXA Display

**Version:** 4.3  **Date:** 2025-10-20
**Provider:** NT Technologies GmbH – powered by NetTask  

---

## 1 Overview

### 1.1 Definition
**HXA Room Booking** is a service of the HXA.io ecosystem that enables organizations to use rooms and shared resources efficiently.  
It consists of:

- **HXA.io Service (Backend & Portal)** – The administrative and integration layer for Microsoft Exchange Online or on-premises environments.  
- **HXA Room Booking App** – A multi-platform client (iOS, Android, Windows, Web) for booking, check-in/out, and visualization of room status.  
- **HXA Display (optional)** – A 10.1" touch device with integrated LED status light and NFC, pre-installed with the Room Booking App and enhanced hardware functions.

### 1.2 Scope of Supply
The vendor provides the HXA.io Service as a cloud service and the HXA Room Booking App as client software.  
The **HXA Display** is optional hardware that can be purchased pre-configured and linked to a defined room resource.

---

## 2 Service Components

### 2.1 HXA.io Service (Backend & Portal)

#### Main Functions
- **Resource Management** – Creation of rooms, assignment of connectors (Microsoft Graph or EWS), device registration.  
- **Device Management** – Linking devices by registration code, central configuration.  
- **Branding** – Room-specific backgrounds, logos, and LED color sets.  
- **Automation & Integration** – Trigger-based automation and control modules (e.g., relays, RGB/W-controllers, smart bulbs).  
- **Monitoring** – Event logs for connector health, authentication, and synchronization status.  

#### Supported Connectors
- **Exchange Online (Microsoft 365)** via **Microsoft Graph**  
  - *Application Connector* (App-only) – Organization-level access.  
  - *Service Connector* (Delegated) – Access via a service account.  
- **Exchange On-Premises (2013 and later)** via **EWS**.  
- Hybrid Exchange environments supported.

---

### 2.2 HXA Room Booking App

#### Availability
- **iOS (iPad)** – via Apple App Store  
- **Android** – via Google Play Store  
- **Windows 10/11** – via Microsoft Store  
- **Progressive Web App (PWA)** or kiosk mode installation also possible.  

#### Functional Highlights
- Quick Meeting (instant booking) and Check-in/Check-out (no-show prevention).  
- Room status display (free / reserved / occupied) and upcoming events.  
- Planning directly on the display or via Outlook/Exchange calendar.  
- Custom branding and background per room.  
- Automatic sync with HXA.io Service and Exchange calendar.  

#### Exchange Integration
Calendar synchronization is handled via Microsoft Graph (Exchange Online) or EWS (Exchange On-Premises), depending on the connector type.  

---

### 2.3 HXA Display (optional)

#### Hardware Specifications
- **Display:** 10.1" touchscreen  
- **LED Status Frame:** full surround, RGB-configurable  
- **NFC:** for user Check-in / Check-out  
- **Connectivity:** Ethernet (PoE), Wi-Fi / Bluetooth  
- **Power:** PoE or 230 V adapter  
- **Mounting:** Wall mount (VESA and flush-mount compatible)  
- **Ports:** DC-In, RJ45, USB/OTG, MicroSD, Earphone, Serial port  
- **Dimensions:** 24.9 × 16.9 × 2.4 cm  

#### Extended App Functions
- Integrated LED control based on booking status (green = free, yellow = about to start, red = occupied).  
- Configurable color profiles per resource via the HXA.io Portal.  
- NFC authentication for meeting check-in/out with user badges or tokens.  

---

## 3 Customer Responsibilities & System Requirements

### 3.1 Microsoft Environment
- **Exchange Online (M365):** Setup of either an Application Connector (App-only) or a Service Connector (Delegated).  
- **Exchange On-Premises (≥ 2013):** Accessible EWS endpoint (HTTPS) and a service account with FullAccess to room mailboxes.  
- **Resource Mailboxes:** Created and configured with booking policies and room lists.  

### 3.2 Network
- Outbound HTTPS (443) to `portal.hxa.io`, `graph.microsoft.com`, `login.microsoftonline.com`, and Exchange/EWS endpoints must be permitted.  

### 3.3 Devices
- Supported clients: iPad, Android tablet, Windows device, or HXA Display unit.  
- Each device requires registration through the HXA.io Portal (resource → add device → enter code).  

### 3.4 NFC Usage
- Customer provides NFC cards/tokens and maintains user-to-tag mapping in compliance with data protection policies.

---

## 4 Provisioning & Operation

### 4.1 Initial Setup
1. Create a Connector (Application or Service).  
2. Create the Room Resource and assign its calendar.  
3. Register the device with the resource using its displayed code.  
4. Configure branding and LED colors if desired.  

### 4.2 Maintenance
- Connector and device status visible via Portal event logs.  
- Automatic software updates for App and Display through HXA.io update service.

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
- Restrict application scope via *Application Access Policies* to defined mailboxes.  
- Prefer `Calendars.ReadBasic.All` for minimum data exposure.  
- Document Admin Consent and limit optional permissions.  

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
| User.Read | Delegated | Sign in and read user profile (Service user context). |
| User.ReadBasic.All | Delegated | Read basic profiles of all users (for name resolution/NFC). |

**Notes & Best Practices**  
- The service user must have FullAccess to the target room mailboxes in Exchange.  
- Apply “least privilege” principle and document Admin Consent.  
- The `offline_access` grant allows continuous operation for unattended devices (Display mode).  

---

## 6 Support and Lifecycle
Support and update services follow NT Technologies’ standard SLA plans.  
Maintenance windows, service availability, and renewal terms are defined per contract.

---

## 7 Legal Notes
“Microsoft”, “Exchange”, “Microsoft 365”, and “Graph” are trademarks of Microsoft Corporation.  
HXA.io and HXA Room Booking are products of **NT Technologies GmbH**, Germany.

---

## Appendix A – Hardware Dimensions & Ports

| Dimension | Value |
|------------|-------|
| Width | 24.9 cm |
| Height | 16.9 cm |
| Depth | 2.4 cm |
| Interfaces | DC-In, RJ45 (Ethernet/PoE), USB/OTG, MicroSD, Earphone, Serial Port |

---

## Appendix B – Device Registration Process

1. Install the HXA Room Booking App on the tablet or use a pre-installed HXA Display.  
2. Launch the App → tap **Register Device** to display the registration code.  
3. Open the HXA.io Portal → select the room resource → **Add Device** → enter the code.  
4. Confirm and verify the synchronization status in the Portal.

---

*© 2025 NT Technologies GmbH – All rights reserved.*