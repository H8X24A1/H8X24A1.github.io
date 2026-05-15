---
label: Reconsent
icon: boot-arrow-clockwise
order: 98
---

# Reconsent a Service Account Connector for HXA.io Door Connect (Microsoft Teams)

## Overview

If the Microsoft Teams connector for **HXA.io Door Connect** requires renewed permissions, a reconsent process must be performed.

You can identify this directly in the **Connectors** page of the HXA.io Portal.

If a reconsent is required, the connector status will display a **red circular arrow icon**. Click this icon to start the reconsent process.

---

## Step 1 – Open the Connector Reconsent

Navigate to:

> **HXA.io Portal → Connectors**

Locate the Microsoft Teams connector for **HXA.io Door Connect**.

If reconsent is required, you will see:

- A **red circular arrow icon**
- Connector status indicating that renewed consent is necessary

Click the icon to continue.

---

## Step 2 – Initial Consent Information

After clicking the reconsent icon, HXA.io will display the following information:

> **To add a Service Account Connector, follow these steps:**  
>
> First, sign in with a Microsoft administrator account to grant consent on behalf of your organization to our application. This initial login is required to authorize access.
>
> After consent is granted, we will display a login code. Enter this code at the Microsoft login URL and sign in with the account you want to use as the service account.

Click continue to open the Microsoft authentication window.

---

## Step 3 – Microsoft Login

A Microsoft login window will open from:

`https://login.microsoftonline.com/`

At this step:

- Use the account that was originally used to grant the first consent for the application
- This is typically an administrator or Azure application administrator account

---

## Step 4 – Admin Approval (if required)

If the selected account does not have sufficient administrator rights, Microsoft will display an elevation request.

Microsoft message example:

> **Need admin approval**  
> HXA.io Door Connect needs permission to access resources in your organization that only an admin can grant. Please ask an admin to grant permission to this app before you can use it.
>
> Have an admin account? Sign in with that account.

In this case:

- Sign in using an administrator account
- The account must have permission to:
  - Grant tenant-wide consent
  - Register or approve enterprise applications in Microsoft Entra ID (Azure AD)

---

## Step 5 – Grant Permissions

Microsoft will now display the permissions requested by **HXA.io Door Connect**.

Example permissions:

- Send channel messages
- Read all groups
- Read the names and descriptions of teams
- Read the names and descriptions of channels
- Read all users' basic profiles
- Read user channel messages
- Maintain access to data you have given it access to
- View users' basic profile

You will also see the option:

> **Consent on behalf of your organization**

### Important

You **must**:

- Enable the checkbox:
  - **Consent on behalf of your organization**
- Then click:
  - **Accept**

This grants the required permissions tenant-wide.

---

## Step 6 – Device Login Information

After successful admin consent, HXA.io will display a device login information window.

Example:

> **Info**  
> Please enter the device code "<device code>" at  
> `https://login.microsoft.com/device`  
> and login with the account you wish to use as the service account.

At this point:

1. Copy the displayed device code
2. Open:

   `https://login.microsoft.com/device`

3. Paste the device code

---

## Step 7 – Authenticate the Service Account

Microsoft will now display:

> **Enter code to allow access**  
> Once you enter the code displayed on your app or device, it will have access to your account.

Continue with:

- The account that should be used as the actual HXA.io Door Connect service account
- This account does **not** need to be the admin account
- It should be the dedicated operational Teams service account

Click:

> **Continue**

---

## Step 8 – Confirm the Application Access

Microsoft will ask:

> **Are you trying to sign in to HXA.io Door Connect?**  
> Only continue if you downloaded the app from a store or website that you trust.

Click:

> **Continue**

---

## Step 9 – Completion

After successful authentication, Microsoft will display:

> **HXA.io Door Connect**  
> You have signed in to the HXA.io Door Connect application on your device. You may now close this window.

The reconsent process is now completed successfully.

---

## Result

The Microsoft Teams service account connector is now:

- Reauthorized
- Connected again to Microsoft Teams
- Ready for operation within HXA.io Door Connect

The connector status in the HXA.io Portal should now return to a healthy state.