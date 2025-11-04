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
It visualizes occupancy and availability data in either a **scrollable list** or an **interactive map view**, providing real-time transparency in office and building environments.

The Room Board connects seamlessly to **Microsoft 365 Graph** and **Exchange Web Services (EWS)** through official **HXA.io Connectors**, supporting **hybrid configurations** that unify data from both cloud and on-premises systems.  
This makes HXA Room Board the ideal solution for **modern workplaces**, **smart offices**, and **digital reception areas**.

---

## 2 Key Features

### 2.1 Multi-Source Booking Display
- Displays real-time booking data from multiple resource types.  
- Supports **hybrid Microsoft environments** (Exchange Online + Exchange On-Premises).  
- Continuously synchronizes data for always up-to-date resource states.

### 2.2 Dual Visualization Modes
- **List View**: Compact, vertically scrollable list of resource bookings.  
- **Map View**: Interactive layout showing rooms, desks, or areas by position and status.

### 2.3 Official Connector Integration
- Uses official **HXA.io-managed connectors**:
  - **Microsoft 365 Graph Connector**
  - **Microsoft Exchange (EWS) Connector**
- Supports mixed operation in hybrid infrastructures.  
- Handles all authentication and synchronization processes automatically.

### 2.4 Weather Integration
- Displays current **weather information** based on the resource or building address.  
- Automatically updates weather data at regular intervals.

### 2.5 Advertising and Informational Content
- Allows display of **images**, **YouTube videos**, and **web content** alongside booking information.  
- Administrators can define **the display duration per media item** (e.g., 10–60 seconds) before automatic rotation.  
- Enables **corporate communication**, **branding**, and **visitor information** directly on the Room Board.  
- Supports smooth transitions between multiple content elements.

### 2.6 Smart Pagination
- Automatically divides long resource lists into multiple pages.  
- Guarantees a clean, readable layout even on smaller displays.

### 2.7 Progressive Web App (PWA)
- Runs as a **Progressive Web App** in modern browsers with app-like behavior.  
- Enables **offline caching**, **auto-refresh**, and **full-screen kiosk mode**.  
- No native installation or platform-specific app required.

---

## 3 Architecture and Data Flow

1. **Connector Setup**  
   Administrators configure backend systems using official HXA.io connectors for Microsoft 365 Graph and/or Exchange EWS.

2. **Resource Synchronization**  
   HXA.io automatically retrieves available resources from connected systems.

3. **Resource Selection**  
   Administrators select which rooms, desks, or workspaces will appear on the Room Board.

4. **Configuration**  
   - Choose between **List View** or **Map View**.  
   - Enable **Weather** and/or **Advertising Content**.  
   - Assign configuration to a display device.

5. **Display Operation**  
   The Room Board continuously updates resource and media data.  
   Pagination and content rotation are managed dynamically.

---

## 4 Microsoft Graph Permissions

**HXA Room Board** uses the same Microsoft Graph permissions as **HXA Room Booking**, ensuring consistent integration and secure data access.

> **Note:** In hybrid setups, Microsoft Graph handles cloud resources while EWS manages on-premises mailboxes.

---

## 5 Setup and Configuration

### 5.1 Prerequisites
- Active **HXA.io Tenant**  
- Configured **Microsoft 365 Graph** and/or **Exchange EWS Connector**  
- Registered display device (HXA Display, iPad, Android Tablet, or Windows PWA client)

### 5.2 Configuration Steps
1. Open **Devices → Room Board** in the HXA.io Admin Center.  
2. Add and authorize one or more connectors.  
3. Select available resources to show.  
4. Choose **List View** or **Map View**.  
5. Optionally enable:
   - **Weather display**  
   - **Advertising and informational content** (with individual duration per item)  
6. Assign configuration to a display device and publish.

### 5.3 Optional Enhancements
- **Map Layout Definition:** Assign coordinate positions to rooms or desks for spatial display.  
- **Weather Data Source:** Uses location from resource metadata for automatic sync.  
- **Media Display Rotation:** Define how long each media item remains visible before transition.

---

## 6 Device Compatibility

**HXA Room Board** runs as a **Progressive Web App (PWA)** and is compatible with multiple platforms and form factors:

| Platform | Supported Environment |
|-----------|------------------------|
| **HXA Display** | Native integration and optimized rendering for lobby and meeting displays |
| **iPad** | Safari or Chrome browser; supports full-screen kiosk mode |
| **Android Tablets** | Chromium-based browsers (Chrome, Edge); kiosk mode compatible |
| **Windows Devices** | Chrome, Edge, or installed as standalone PWA |
| **Smart Displays / Info Screens** | Any device with a Chromium-compatible browser |

> The Room Board automatically adjusts its layout based on screen size, orientation, and touch capability.

---

## 7 Summary

**HXA Room Board** is the intelligent display surface of the HXA.io Platform — merging **room visibility**, **environmental context**, and **informational media** into one adaptive PWA experience.  
By unifying Microsoft 365 and Exchange data, integrating weather and custom content, and running seamlessly across multiple device types, it delivers a transparent, flexible, and engaging interface for **smart workplaces and digital buildings**.

## 8 Support & Lifecycle

Service availability, updates, and SLAs follow NT Technologies’ standard support policy.

---