---
title: Create and manage workspaces - Microsoft Exchange - HXA.io DOCS
label: Create and manage workspaces
icon: paste
order: 100
---
# Creating and manage a Microsoft Workspace Resource using PowerShell and Exchange Online Admin Center

Microsoft Workspace Resources are useful for managing shared spaces like meeting rooms, workspaces, and other resources in an organization. By creating a workspace resource, you can manage bookings and reservations in Outlook Online. In this guide, we will walk you through the process of creating a Microsoft Workspace Resource in Exchange Online using both PowerShell commands and the Exchange Online Admin Center.

Before you begin, make sure you have the following:

Admin access to the Exchange Online Admin Center.
PowerShell with the Exchange Online Management module installed.
Global admin or Exchange admin permissions in your organization.

## Creating a Microsoft Workspace Resource using Exchange Online Admin Center (EOAC)

1. Access the Exchange Online Admin Center:
Log in to your Microsoft 365 admin account and navigate to the Exchange Online Admin Center (EOAC) by clicking on "Admin centers" and then "Exchange". Or go to https://admin.exchange.microsoft.com and sign in with your admin credentials.

2. Create the Workspace resource:
In the EOAC, go to "Recipients" in the left-hand menu, and then click on the "Resources" tab.

3. Click on the "+" icon and select either "Room mailbox" or "Equipment mailbox", depending on the type of Workspace resource you want to create.

4. Fill in the required information:
Provide a name, email address, capacity (if applicable), and any other relevant information for the new Workspace resource. Click on "Save" to create the resource.

5. Configure additional settings:
Once the resource is created, you can click on it in the Resources list to access and configure additional settings, such as booking options, delegate permissions, and custom properties.

6. Configure Workinghours via Powershell
    Configuring working hours for a workspace, particularly in Microsoft Exchange, helps align calendars and schedules with the actual working times of your organization or team members. This ensures that scheduling tools, like Microsoft Outlook or Teams, display accurate availability for meetings and events, which helps streamline internal and external communication.

    To configure working hours, Microsoft Exchange provides the Set-MailboxCalendarConfiguration PowerShell cmdlet. This command allows administrators to customize individual mailbox settings, including working hours. Here's a brief overview of how you can achieve this:

    Install PowerShell Module: Ensure you have the Exchange Online PowerShell module installed.
    Connect to Exchange Online: Use PowerShell to establish a session with Exchange Online.
    Set Working Hours: Execute the Set-MailboxCalendarConfiguration cmdlet for the mailbox you intend to configure. You can set working hours by using the WorkHoursStartTime, WorkHoursEndTime, WorkingDays, and other parameters.

    Here's a sample command to configure working hours:
    ```powershell
    Set-MailboxCalendarConfiguration -Identity user@domain.com -WorkHoursStartTime 08:00 -WorkHoursEndTime 17:00 -WorkingDays Monday, Tuesday, Wednesday, Thursday, Friday
    ```
    [!ref Set-MailboxCalendarConfiguration](https://learn.microsoft.com/en-us/powershell/module/exchange/set-mailboxcalendarconfiguration?view=exchange-ps)



!!!
Don't forget to assign the workspace mailbox to a room list that it will come available to select this workspace calendar in [!ref target="blank" text="HXA.io Portal"](https://hxa.io/)  - Resource Management. Please notice that it can take up to 24 hours that the workspace can be used and w displayed in the calendar selection of the HXA Resource Management.
!!!



## Use Exchange  PowerShell to create a room mailbox in Exchange OnPremise or Exchange Online

Connect to Exchange Online PowerShell:
Before you can create a Workspace resource using PowerShell, you need to connect to Exchange Online. Replace the placeholders with your desired values, and then run the following command:

```powershell
# Install Exchange Online Management module if not already installed
Install-Module -Name ExchangeOnlineManagement

# Import Module
Import-Module ExchangeOnlineManagement

# Connect to Exchange Online
Connect-ExchangeOnline
```
### Create the Workspace Resource.

```powershell
New-Mailbox -Name "<WorkspaceName>" -Alias "<WorkspaceAlias>" -OrganizationalUnit "example.com/Users" -Room -RoomMailboxPassword (ConvertTo-SecureString -String "<Password>" -AsPlainText -Force) | Set-Mailbox -type Workspace
```

For example:
```powershell
New-Mailbox -Name "Workspace A" -Alias "workspaceA" -OrganizationalUnit "example.com/Users" -Room -RoomMailboxPassword (ConvertTo-SecureString -String "P@ssw0rd" -AsPlainText -Force) | Set-Mailbox -type Workspace
```

### Set the Workspace Resource properties.

```powershell
Set-CalendarProcessing -Identity "<WorkspaceAlias>" -AutomateProcessing AutoAccept -DeleteComments $false -DeleteSubject $false -AddOrganizerToSubject $true -AllowConflicts $false  -ResourceCapacity "<capacity>"
```

For example:
```powershell
Set-CalendarProcessing -Identity "workspaceA" -AutomateProcessing AutoAccept -DeleteComments $false -DeleteSubject $false -AddOrganizerToSubject $true -AllowConflicts $false  -ResourceCapacity 10
```