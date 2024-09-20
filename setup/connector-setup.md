---
label: Connector Setup
icon: repo-forked
order: 900
---

There are three types of connectors in HXA.io products to connect to Microsoft services:
- Microsoft Exchange OnPremise (via EWS)
- Microsoft Exchange Online (Office 365) [Supported Types: Application or Service]
- Microsoft Entra ID [Supported Types: Application]
- Microsoft Teams [Supported Types: Service]

## Microsoft Exchange Online (Office 365)
There are two types of connectors to connect to Microsoft Exchange Online (Office 365):
- via Microsoft Office 365 Application account or
- via Microsoft Office 365 Service account with Application Impersonation Role Setuped

### Setup via Microsoft Office 365 Application account

Connecting the HXA.io Connector as an installed application using an application account is a very easy setup that you don't have to worry about later. This method, which requires an account with the Global Administrator role, installs an application for HXA.io for the entire Microsoft Office 365 tenant. The benefit of this is that you don't have to worry about keeping permissions up to date when adding new resource mailboxes, for example.

Use a Microsoft 365 application account to access all information and accounts within your organization with a single connector.

- To do this, log in to the HXA.io portal at https://portal.hxa.io.
- Open the menu item "Settings" -> "Connectors".
- Connect an Office 365 connector and select the type application account.
- A window then opens asking you to authenticate using a Microsoft account.

!!!
Please note that the account used for authentication must have Global Administration permissions with in the organization in order to grant access authorization for an application account.
!!!

### Setup via Microsoft Office 365 Service account

A Service account offers more configuration options and makes sense for organizations that want the highest level of control (e.g. over permissions, logs, etc.). The service account should have Application Impersonation access to all room calendars to be managed within the HXA.io tenant.

Use a Microsoft 365 user/service account if you want to authorize a single connector to access custom and shared calendars.

- To do this, log in to the HXA.io portal at https://portal.hxa.io.
- In the menu, open "Settings" -> "Connectors"
- Connect an Office 365 connector and select the type User/Service account.
- A window then opens asking you to authenticate using a Microsoft account.
