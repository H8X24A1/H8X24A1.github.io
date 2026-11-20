---
label: Getting Started
icon: rocket
order: 900
title: HXA.io Getting Started Guide
description: Learn how to set up HXA.io with Microsoft 365, Exchange Online or On-Premise, and configure connectors for room booking, workplace management, and building automation.
---

# Getting Started

## What is HXA.io?

HXA.io is a user-centric Building Operating System for commercial buildings.  
It connects Microsoft 365, room and workplace booking, resource management, access systems, displays, and building automation into one unified platform.

## What this guide covers

This documentation helps administrators to install and configure HXA.io applications and services step by step.

It includes:

- Connecting Microsoft 365 (Exchange Online)
- Connecting Microsoft Exchange On-Premise (Hybrid scenarios)
- Setting up connectors in the HXA.io Portal
- Preparing resources like rooms, workplaces, and other bookable assets

## Requirements

Before starting, ensure the following:

- Internet connectivity for all HXA.io components
- A calendar host appropriate for your setup: HXA.io-hosted calendars, Microsoft 365, or an Exchange environment
- Permissions for the relevant HXA.io portal areas and, when connecting Microsoft services, an account authorized for the required setup and consent
- Access to the HXA.io Portal: https://portal.hxa.io

## System architecture overview

Choose the connection model that matches the resource:

| Calendar connection | Setup |
| --- | --- |
| HXA-hosted calendar | HXA.io Local Connector and the Calendars area in the portal |
| Microsoft 365 room or equipment mailbox | Microsoft Office 365 Resources connector using Microsoft Graph |
| Exchange calendar through the portal | Microsoft Exchange connector using EWS |
| Direct access from an HXA Display to an on-premises Exchange server | Optional local EWS connection add-on, configured on the display |

In the direct display-to-Exchange mode, calendar data is exchanged locally; HXA.io Services remain involved in function settings, configuration, and licensing. See [Local Exchange Connection via EWS](/setup/connector-setup/microsoft-exchange/local-ews-connection.md).

The **HXA.io Local Connector** is the portal's calendar-host option. Its name does not refer to the display's local Exchange connection.

## Setup process (high-level)

The setup is performed centrally via the HXA.io Portal.

Main steps:

1. Create an HXA.io account at https://portal.hxa.io  
2. Choose the calendar host and configure the connectors required by the applications you use. Microsoft Entra ID supports directory integration and the floor-plan links editor; Teams connectors are used for Door Connect workflows.
3. Complete the required Microsoft authorization when connecting Microsoft services.
4. Import users if required and assign the appropriate user licenses.
5. Configure resources, their calendars, resource licenses, and devices.
6. Configure application options and verify the result on the intended clients.

## Next steps

Continue with the documentation for your setup:

- [Portal Navigation](/setup/portal-navigation.md)
- [Connector Setup](/setup/connector-setup/connector-setup.md)
- [Calendar Setup](/setup/calendar-setup.md)
- [User Management](/setup/user-setup.md)
- [Room Booking Resource Configuration](/setup/resource-setup/room-booking-setup/resource-setup.md)
- [License Assignment](/license/assign-license.md)
- [Local Exchange Connection via EWS](/setup/connector-setup/microsoft-exchange/local-ews-connection.md)

<!-- Connection choices and portal navigation checked on 2026-11-20, P01, P03, P11, P12. Storage, caching, and retention policies cannot be inferred from these UI observations. -->
