---
label: Role Setup
icon: shield
order: 95
description: Find and configure HXA.io portal roles and their permissions.
---

# Role Setup

Open **Account > Roles** in the [HXA.io Portal](https://portal.hxa.io). **Role management** provides **Create role**, a search field, and a table with **Name** and **Options**.

## Review a role

1. Find the role in the overview.
2. Open its **Options** menu and choose **Edit role**, when available.
3. Review the **User Role Permissions** page and expand the relevant section under **Portal Permissions**.

The **Admin** role's Edit role and Delete role actions are disabled in the inspected portal. Other roles can expose an editable permission form. Role names created within an organization are not a universal set of default roles.

## Permission areas

| Area | Sections in the role form |
| --- | --- |
| People and access | User permissions, Group permissions, Role permissions |
| Devices and resources | Device Permissions, Connector Permissions, Resource Permissions, Floor Plan permissions, calendars |
| Organization and licensing | Organization Profile Permissions, Invoice permissions, License Permissions, Payment Method Permissions, Subscription permissions |
| Services and content | Room Demands Permissions, News Stream Permissions |
| Automation | Trigger Permissions, Automation Portal Permissions, Control Module Permissions, MQTT Permissions |

For example, **User permissions** contains separate **Show users**, **Create users**, **Edit users**, and **Delete users** checkboxes. Review each area individually rather than assuming that viewing an object also grants permission to change it.

The calendars heading may appear as `permissions.Calendars.TITLE` in the English interface.

## Save and assign

After intentionally changing a role, use **Save**. Assign the role to the appropriate profile under **Account > Users > Edit user > PERMISSIONS**.

Verify the intended access with an account assigned to that role. The permission form alone does not demonstrate which pages or actions that account can actually use.

<!-- Source: authenticated portal inspection, 2026-11-20, P09. No role was created, saved, or assigned; effective permissions were not tested. -->
