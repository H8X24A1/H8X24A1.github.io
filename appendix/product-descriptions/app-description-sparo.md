# HXA Sparo – Application Service

**Version:** 3.8  **Date:** 2025-10-20
**Provider:** NT Technologies GmbH – powered by NetTask  

---

## 1 Overview

### 1.1 Definition

**HXA Sparo** is the **mobile-first workspace booking application** of the HXA.io ecosystem.  
It enables intuitive, fast, and intelligent reservation of desks, rooms, shared spaces, as well as parking spaces — seamlessly integrated with Microsoft 365 / Exchange calendars.

Sparo combines a **personalized dashboard** (news, weather, working hours, maps, daily bookings) with an **AI-driven Booking Assistant**, providing an adaptive, branded, and ecological booking experience.

### 1.2 Scope of Supply

The vendor provides:

- **HXA.io Service (Backend & Portal)** – Administration, connectors, users/licensing, resources, maps, branding, and monitoring.  
- **HXA Sparo App** – Mobile and PWA client for booking, check-in, and interactive dashboard with news, weather, location, working hours, and daily bookings.  
- **Optional Modules** – Map Drawing Engine for visual resource linking, and the AI-based Booking Assistant.

---

## 2 Service Components

### 2.1 HXA.io Service (Backend & Portal)

#### Main Functions

- **Connector Management** – Minimum two connectors required:
  1. **Microsoft Entra ID (Azure AD)**  
  2. **Microsoft Office 365 Resources (Graph)**  
  *(optional)* **Microsoft Exchange Sparo (EWS)** for Hybrid/On-Prem Exchange
- **Resource Management** – Create and configure rooms/desks; link to mailboxes; define capacity, window orientation, equipment; manage QR codes.  
- **User & License Management** – Import Microsoft 365 users via Entra ID; assign Sparo licenses; manage roles.  
- **Branding & Dashboard** – Upload company logo, activate news, weather, working hours, location, and daily booking widgets.  
- **News Publishing** – Create company news that appears directly on the Sparo Dashboard.  
- **Map Drawing & Linking** – Upload and manage building/floor maps; place symbols or shapes and link them with resources for visual booking.  
- **Automation & Logs** – Connector health, synchronization, and authentication monitoring.

#### Supported Connectors

- **Microsoft Entra ID (Azure Active Directory)** – Identity and user import.  
- **Microsoft Office 365 Resources (Graph)** – Access to calendars, users, places, mailbox settings.  
- **Microsoft Exchange Sparo (EWS)** – *Optional*, for Hybrid or On-Prem Exchange.  
  *(Sparo targets Exchange Online primarily via Graph.)*

---

### 2.2 HXA Sparo App

#### Availability

- **Mobile (primary):** iOS and Android – fully optimized for smartphones.  
- **Web (PWA):** Windows/macOS – modern browsers.

#### Functional Highlights

- **Dashboard Modules:**
  - 📰 **Company News** – from HXA.io News stream.  
  - ☀️ **Weather Widget** – displays local forecast for the user’s current location.  
  - 🏢 **Company Logo / Branding** – tenant-specific header and color scheme.  
  - 🕒 **Working Hours** – from Microsoft 365 mailbox settings or tenant defaults.  
  - 📍 **Location Tile** – displays building/floor assignment from HXA Maps or user profile.  
  - 📅 **Today’s Bookings** – lists daily bookings with quick actions (check-in, extend, cancel).  
  - 🗺️ **Interactive Map View** – displays floor and building maps with clickable symbols representing resources.  
    - Tap a symbol to **book instantly** or schedule a time slot.  
    - Occupied resources show the **Organizer** and **Subject**, giving quick context.  
    - Helps users visualize building occupancy and navigate efficiently.

- **Real-time availability** and **capacity view** for each resource.  
- **Fast booking** (time-boxed or all-day) and **My Bookings** with live status.  
- **QR Code Check-In** – instant reservation/check-in.  
- **Favorites** – quickly access preferred desks/rooms.  
- **Booking Assistant** – recommends best-fit resources (see point 2.2.1).

---

### 2.2.1 Booking Assistant

The **AI-based Booking Assistant** recommends optimal resources by analyzing:

| Category | Example Signals |
|-----------|-----------------|
| Hard Requirements | capacity, time, equipment, window orientation |
| Historical Preferences | previous bookings, feedback, user satisfaction |
| Context | group/team membership, relevant colleagues (Graph People), office location |
| Ecological Fit | energy-efficient zones, floor clustering to reduce HVAC/light usage |

The assistant ranks all available resources and presents explainable suggestions such as:  
> “Closest to your team”, “Your usual workspace on Floor 2”, or “Energy-optimized zone”.

---

### 2.3 HXA Display (optional)

Optional display panel to complement room signage or reflect the same map view and dashboard widgets (weather, logo) when combined with **HXA Room Booking**.

---

## 3 Customer Responsibilities & System Requirements

### 3.1 Microsoft Environment

To run Sparo:

1. **Create connectors** for Entra ID and Office 365 Resources (Graph).  
2. *(Optional)* Add Exchange Sparo (EWS) for Hybrid/On-Prem.  
3. **Import users** from Entra ID and **assign HXA Sparo licenses**.

### 3.2 Network

Allow HTTPS (443) traffic to:
- `portal.hxa.io`
- `graph.microsoft.com`
- `login.microsoftonline.com`
- Exchange/EWS (Hybrid)

### 3.3 Devices

- iOS/Android smartphones (latest two OS generations)  
- PWA on Windows/macOS  
- Camera access required for QR check-in
- Location access reqquired for Maps location

### 3.4 Map Drawings

- Supported formats: **SVG** (recommended) and **PNG**  
- Maps may represent **buildings**, **floors**, or **spaces**  
- Admins can link resources via **symbols or shapes**  
- In the app, users can tap the symbol to:
  - Make a **Quick Booking** or **Scheduled Booking**  
  - View **Organizer** and **Subject** info for existing bookings  
- The graphical layout improves orientation and occupancy overview.

### 3.5 QR Usage

Each resource must have a unique, visible QR code linked to its calendar identity.

---

## 4 Provisioning & Operation

### 4.1 Initial Setup

1. Create connectors (Entra ID + Office 365 Resources, optionally EWS).  
2. Import users from Entra ID.  
3. Assign HXA Sparo licenses.  
4. Create resources and link to mailboxes.  
5. Upload maps and link resources using shapes/symbols.  
6. Configure dashboard (news, weather, working hours, location).  
7. Enable and tune Booking Assistant (eco-rules, weights).  
8. Deploy QR codes and communicate app/PWA rollout.

### 4.2 Day-to-day Operations

- Manage users/licenses, news, branding, maps, and resources in HXA.io.  
- Monitor connector health and event logs.  
- Mobile apps update via stores; PWA refreshes automatically; backend updated by HXA.io.

---

## 5 Security & Microsoft Graph Permissions

Sparo uses **Microsoft Graph API** and **Microsoft Entra ID OIDC** for authentication and data access.

### 5.1 Authentication Flows

- **Authorization Code with PKCE** – for PWA/native mobile login.  
- **Client Credentials** – for app-only connector operations.  
- Optional **offline_access** scope for persistent sign-in.

### 5.2 Microsoft Graph permissions used by HXA Sparo

The following Microsoft Graph permissions are required by HXA Sparo.  
They vary depending on the connector type (Application or Delegated).  
**Admin consent** is required where indicated as *Yes*.

| API / Permissions name | Type | Description | Admin consent required |
|-------------------------|------|--------------|------------------------|
| Calendars.Read | Application | Read calendars in all mailboxes | Yes |
| Calendars.Read | Delegated | Read user calendars | No |
| Calendars.Read.Shared | Delegated | Read user and shared calendars | No |
| Calendars.ReadBasic.All | Application | Read basic details of calendars in all mailboxes | Yes |
| Calendars.ReadWrite | Application | Read and write calendars in all mailboxes | Yes |
| Calendars.ReadWrite.Shared | Delegated | Read and write user and shared calendars | No |
| Directory.Read.All | Application | Read directory data | Yes |
| Directory.ReadWrite.All | Application | Read and write directory data | Yes |
| Group.Read.All | Delegated | Read all groups | Yes |
| Group.ReadWrite.All | Delegated | Read and write all groups | Yes |
| GroupMember.Read.All | Delegated | Read group memberships | Yes |
| GroupMember.ReadWrite.All | Delegated | Read and write group memberships | Yes |
| Mail.Read | Application | Read mail in all mailboxes | Yes |
| Mail.ReadWrite | Application | Read and write mail in all mailboxes | Yes |
| MailboxSettings.Read | Delegated | Read user mailbox settings | No |
| MailboxSettings.ReadWrite | Application | Read and write all user mailbox settings | Yes |
| openid | Delegated | Sign users in | No |
| People.Read | Delegated | Read users’ relevant people lists | No |
| Place.Read.All | Delegated | Read all company places | Yes |
| Place.Read.All | Application | Read all company places | Yes |
| Place.ReadWrite.All | Delegated | Read and write organization places | Yes |
| profile | Delegated | View users’ basic profile | No |
| Schedule.Read.All | Application | Read all schedule items | Yes |
| Schedule.ReadWrite.All | Application | Read and write all schedule items | Yes |
| User.Read | Delegated | Sign in and read user profile | No |
| User.Read.All | Application | Read all users’ full profiles | Yes |
| User.ReadBasic.All | Delegated | Read all users’ basic profiles | No |
| User.ReadWrite.All | Delegated | Read and write all users’ full profiles | Yes |

**Notes:**
- *Application permissions* are used by the **HXA.io backend connector** (app-only mode).  
- *Delegated permissions* are used by **service connectors** operating on behalf of a user or service account.  
- Always apply **Application Access Policies** or **RBAC for Applications** to restrict app-only access to specific resource mailboxes.  
- Sparo uses the **Authorization Code Flow with PKCE** for PWA/native sign-ins and the **Client Credentials Flow** for background connector operations.  
- The optional `offline_access` scope may be enabled where persistent sessions are required.

> Apply **least privilege** and limit app-only access using **Application Access Policies** or **RBAC for Applications**.

---

## 6 Backend & Integration Dependencies

- **Microsoft Entra ID** – Authentication and directory.  
- **Microsoft Graph** – Calendars, MailboxSettings, Users, Places, People.  
- **Exchange Web Services (EWS)** – Optional hybrid connector.  
- **HXA.io** – Portal for news, branding, maps, monitoring.

---

## 7 Support & Lifecycle

Service availability, updates, and SLAs follow NT Technologies’ standard support policy.

---

## Appendices

### A – Dashboard Widgets & Data Sources

| Widget | Data Source | Description |
|---------|--------------|--------------|
| News | HXA.io News Module | Internal company announcements |
| Weather | External API + Maps Location | Local forecast for user’s current site |
| Logo / Branding | HXA.io Portal | Custom logo and theme colors |
| Working Hours | Microsoft Graph MailboxSettings | Shows user’s defined working hours |
| Location | HXA Maps / User Profile | Displays building / floor assignment |
| Daily Bookings | Microsoft Graph CalendarView | Lists today’s meetings/bookings |
| Interactive Map | HXA Maps Module | Visual overview; Quick/Scheduled Booking |
| Organizer/Subject | Graph Calendar | Displays organizer info on booked spaces |

---

### B – Map Drawing Engine

- Upload custom **SVG/PNG** floor or building maps.  
- Assign resources via **clickable shapes or icons**.  
- Real-time overlay indicates booked (red) vs. free (green) resources.  
- Interactive tap opens:
  - **Quick Booking** (instant reservation)  
  - **Schedule Booking** (select time slot)  
  - **Booking Info** (Organizer, Subject, duration)  
- Graphical layout supports navigation and visual occupancy awareness.

---

### C – Booking Assistant Scoring Model

| Layer | Example Factors |
|--------|-----------------|
| Constraints | Time, capacity, required features |
| Preferences | Historic booking patterns |
| Context | Team proximity, building, people |
| Ecological | Energy cluster efficiency |

---

### D – Quick-Start Checklist

- [ ] Create Connectors (Entra ID + O365 Resources + optional EWS)  
- [ ] Import Users & Assign Licenses  
- [ ] Upload Maps and Link Resources  
- [ ] Configure Dashboard (News, Weather, Logo, Working Hours, Location)  
- [ ] Enable Booking Assistant & Eco Rules  
- [ ] Deploy QR Codes and Communicate Access  

---

*© 2025 NT Technologies GmbH – All rights reserved.*
