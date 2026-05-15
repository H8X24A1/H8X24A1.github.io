---
label: Required permissions
icon: boot-file-break
order: 90
---

# Microsoft Teams Connector Required Permissions for HXA.io Door Connect

## Overview

HXA.io Door Connect integrates with Microsoft Teams to provide communication workflows for chat-based and call-based scenarios.

Depending on the selected connector type, different Microsoft Graph permissions are required.

HXA.io Door Connect currently supports the following Microsoft Teams connector types:

- **Door Connect – Chat Agent**
- **Door Connect – Call Agent**

Each connector type only requests the permissions required for its operational purpose.

---

# Connector Types

## Door Connect – Chat Agent

The Chat Agent is used for Microsoft Teams messaging and channel-based communication workflows.

Typical use cases include:

- Sending Teams messages
- Channel-based notifications
- Communication workflows
- Team and channel interaction

The Chat Agent uses the connector type:

> **User/Service Account**

---

## Door Connect – Call Agent

The Call Agent is used for Microsoft Teams calling workflows.

Typical use cases include:

- Teams call handling
- Call routing
- Call transfer
- Door communication scenarios
- Teams-based calling interactions

The Call Agent uses the connector type:

> **Teams Calling Agent (User/Service Account)**

---

# Required Permissions – Chat Agent

The following permissions may be requested for the Chat Agent connector.

| Permission | Description |
|---|---|
| Send channel messages | Allows the connector to send messages into Microsoft Teams channels |
| Read all groups | Allows discovery of Microsoft 365 groups and Teams structures |
| Read the names and descriptions of teams | Allows access to Microsoft Teams metadata |
| Read the names and descriptions of channels | Allows access to channel metadata |
| Read user channel messages | Allows interaction with Teams channel messaging workflows |
| Read all users' basic profiles | Allows user identification and lookup |
| View users' basic profile | Allows the connector to identify the signed-in account |
| Maintain access to data you have given it access to | Allows persistent connector access without repeated manual sign-ins |

---

# Required Permissions – Call Agent

The following permissions may be requested for the Call Agent connector.

| Permission | Description |
|---|---|
| Manage calls in Teams | Allows the connector to start, join, transfer, forward, and manage Teams calls |
| Manage chats in Teams | Allows interaction with Teams chat threads required for call-related workflows |
| Maintain access to data you have given it access to | Allows persistent connector access without repeated manual sign-ins |
| View your basic profile | Allows the connector to identify the signed-in account |

---

# Administrator Consent

Depending on the Microsoft tenant configuration, administrator approval may be required.

During setup or reconsent, Microsoft may display an administrator approval request.

In this case, a Microsoft administrator must:

1. Sign in with an administrator account
2. Review the requested permissions
3. Enable:

   > **Consent on behalf of your organization**

4. Click:

   > **Accept**

Without the required consent, the connector may not function correctly.

---

# Recommended Security Approach

For production environments, we strongly recommend using dedicated service accounts.

## Recommended Setup

| Connector Type | Recommended Account |
|---|---|
| Door Connect – Chat Agent | Dedicated Teams chat service account |
| Door Connect – Call Agent | Dedicated Teams calling service account |

This approach helps to:

- Apply the least privilege principle
- Separate calling and messaging workflows
- Improve auditability
- Simplify troubleshooting
- Improve operational transparency
- Simplify reconsent handling

---

# Important Notes

## Permissions Depend on the Connector Type

The requested Microsoft permissions depend on the selected connector type.

Not every connector requires the same Microsoft Graph scope.

---

## Microsoft May Change Permission Labels

Microsoft can rename or reorganize permission labels over time.

The displayed wording inside the Microsoft consent dialog may therefore slightly differ depending on:

- Microsoft tenant version
- Microsoft Graph updates
- Microsoft Entra changes
- Regional settings

---

## Permissions Are Displayed During Consent

The currently requested permissions are always displayed directly inside the Microsoft consent window during:

- Initial setup
- Reconsent
- Connector recreation

Administrators should review the displayed permissions before accepting the consent request.

---

# Related Documentation

- Microsoft Teams Connector Initial Setup
- Door Connect Service Account Reconsent
- Door Connect Chat Agent Setup
- Door Connect Call Agent Setup
- Connector Troubleshooting