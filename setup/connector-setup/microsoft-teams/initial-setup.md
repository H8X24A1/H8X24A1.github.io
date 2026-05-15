---
label: Initial Setup
icon: repo-forked
order: 100
---

# Microsoft Teams Connector Initial Setup for HXA.io Door Connect

## Overview

HXA.io Door Connect uses Microsoft Teams to support communication workflows between door stations, visitors, users, and Teams users.

The Microsoft Teams connector can be configured in two different modes:

- **User/Service Account**  
  Used for the Door Connect Chat Agent.

- **Teams Calling Agent (User/Service Account)**  
  Used for the Door Connect Call Agent.

Both connector types follow the same general setup flow. The required Microsoft permissions depend on the selected connector type and can be reviewed in the dedicated permissions documentation.

For details, see:

> **Microsoft Teams Connector Required Permissions**

---

# Open the Microsoft Teams Connector Setup

In the HXA.io Portal, go to:

> **Connectors → Add Connector**

Select:

> **Office 365 – Teams**

You will see two available connector options:

- **User/Service Account**
- **Teams Calling Agent (User/Service Account)**

Choose the connector type you want to configure and click:

> **Connect**

---

# Connector Types

## Door Connect – Chat Agent

Select:

> **User/Service Account**

The Chat Agent is used for Microsoft Teams messaging and channel-based workflows.

It enables HXA.io Door Connect to use a dedicated Microsoft Teams account for chat-based communication scenarios.

---

## Door Connect – Call Agent

Select:

> **Teams Calling Agent (User/Service Account)**

The Call Agent is used for Microsoft Teams calling workflows.

It enables HXA.io Door Connect to use a dedicated Microsoft Teams account for call-based communication scenarios.

---

# General Setup Flow

The setup flow is generally the same for both connector types.

## Step 1 – Select the Connector Type

On the **Office 365 – Teams** connector page, select one of the following options:

- **User/Service Account**
- **Teams Calling Agent (User/Service Account)**

Then click:

> **Connect**

---

## Step 2 – Sign in with Microsoft

A Microsoft login window opens from:

```text
https://login.microsoftonline.com/
```

Sign in with the Microsoft account that should be used for the connector.

For production environments, we recommend using a dedicated service account.

---

## Step 3 – Review the Consent Request

Microsoft displays a consent request for **HXA.io Door Connect**.

The requested permissions depend on the selected connector type.

The detailed permission scope is documented separately.

For details, see:

> **Microsoft Teams Connector Required Permissions**

---

## Step 4 – Accept the Consent Request

After reviewing the Microsoft consent request, click:

> **Accept**

If administrator approval is required, sign in with a Microsoft administrator account and approve the consent request.

---

## Step 5 – Connector Created

After successful Microsoft authentication and consent, the connector is created in HXA.io.

The connector can now be used by HXA.io Door Connect.

---

# Recommended Account Setup

For secure and transparent operation, we recommend using dedicated service accounts.

| Connector Type | Recommended Account |
|---|---|
| Door Connect – Chat Agent | Dedicated Teams chat service account |
| Door Connect – Call Agent | Dedicated Teams calling service account |

This separation helps to:

- Separate messaging and calling workflows
- Apply the least privilege principle
- Simplify troubleshooting
- Make consent and reconsent processes easier
- Improve operational transparency

---

# Important Notes

## Use a Dedicated Service Account

Do not use a personal user account for productive Door Connect integrations.

A dedicated service account provides better:

- Stability
- Auditability
- Lifecycle management
- Permission control

---

## Administrator Approval May Be Required

Depending on the Microsoft tenant configuration and the selected connector type, administrator approval may be required.

If Microsoft displays an admin approval request, an administrator must approve the request before the connector can be used.

---

## Permissions Are Documented Separately

This page describes the initial setup process.

The Microsoft permission scopes are maintained in a separate documentation page to keep setup instructions clear and easy to follow.

For details, see:

> **Microsoft Teams Connector Required Permissions**

---

# Result

After successful setup, the Microsoft Teams connector is available in HXA.io.

Depending on the selected connector type, it can now be used for:

- Door Connect chat workflows
- Door Connect calling workflows

The connector status should show as active and healthy in the HXA.io Portal.

---

# Related Documentation

- Microsoft Teams Connector Required Permissions
- Door Connect Service Account Reconsent
- Door Connect Chat Agent Setup
- Door Connect Call Agent Setup
- Connector Troubleshooting