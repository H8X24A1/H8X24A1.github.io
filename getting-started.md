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
- Access to a Microsoft 365 tenant or Exchange environment
- Global Administrator permissions (for initial setup)
- Access to the HXA.io Portal: https://portal.hxa.io

## System architecture overview

HXA.io does not store Microsoft 365 data independently.  
Instead, it connects directly to Exchange resources and synchronizes data in real time.

This ensures:

- No data duplication
- Real-time booking updates
- Native integration with Outlook and Microsoft Teams

## Setup process (high-level)

The setup is performed centrally via the HXA.io Portal.

Main steps:

1. Create an HXA.io account at https://portal.hxa.io  
2. Configure required connectors:
   - Microsoft Office 365 Resources
   - Microsoft Entra ID (Azure AD)
   - Microsoft Teams Chat/ Call
3. Grant admin consent for the application
4. Import users from Microsoft 365
5. Configure resources (rooms, workplaces, etc.)

## Next steps

#Continue with:

#- [Connector Setup](../connectors/)
#- [User Management](../users/)
#- [Resource Configuration](../resources/)