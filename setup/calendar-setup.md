---
label: Calendar Setup
icon: calendar
order: 850
description: Understand HXA-hosted calendars and find calendar-to-resource assignments in the portal.
---

# Calendar Setup

Calendar hosting and resource configuration are separate choices. The portal offers an **HXA.io Local Connector** for HXA-hosted calendars, alongside connectors for Microsoft services.

For room calendars in Microsoft 365 or Exchange, see [Connector Setup](/setup/connector-setup/connector-setup.md). Direct calendar access from an HXA Display to an on-premises Exchange server is described in [Local Exchange Connection via EWS](/setup/connector-setup/microsoft-exchange/local-ews-connection.md).

## Calendar overview

Open **Calendars** in the [HXA.io Portal](https://portal.hxa.io). Use **Search**, **Filter**, and **Columns option** to inspect entries.

| Column | Information |
| --- | --- |
| Display name | Name shown for the calendar |
| UPN | Calendar identity |
| Resource | Linked HXA resource, where assigned |
| Connector Type - user | Connector/account context |

## Start calendar creation

**Create calendar** opens a form beginning with the required **Select Connector** field. Choose the intended calendar host before continuing with the fields offered for that connector. **Save** is initially disabled until the required information is supplied.

The availability of a connector in this selection does not establish that the same creation workflow is supported for every calendar host. For Microsoft room mailboxes, follow the relevant [Microsoft resource setup](/setup/microsoft-setup/create_room-mailbox.md).

## Check the resource assignment

In **Resources**, open **Options > Edit Resource** for the intended Room Booking resource. Review its **Connector** and **Calendar** sections. Check that both belong to the intended calendar host.

See [Room Booking Resource Setup](/setup/resource-setup/room-booking-setup/resource-setup.md) for the remaining application and device settings.

<!-- Sources: authenticated portal inspection, 2026-11-20, P03 and P11. Creation beyond connector selection could not be verified; complete connector-specific form fields and an end-to-end creation example remain editorial follow-up. -->
