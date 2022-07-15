---
title: Create and manage room mailboxes - Microsoft Exchange - HXA.io DOCS
label: Create and manage room mailboxes
icon: paste
order: 100
---
# Create and manage room mailboxes

## Use the Classic Exchange admin center to create a room mailbox

1. In the Classic Exchange admin center, navigate to Recipients > Resources.
2. To create a room mailbox, click New Add Icon. > Room mailbox.
3. Use the options on the page to specify the settings for the new resource mailbox.
  - Room name: Use this box to type a name for the room mailbox. This is the name that's listed in the resource mailbox list in the Classic Exchange admin center and in your organization's address book. This name is required and it can't exceed 64 characters.
  - Email address: A room mailbox has an email address so it can receive booking requests. The email address consists of an alias on the left side of the @ symbol, which must be unique in the forest, and your domain name on the right. The email address is required.
  - Location, Phone, Capacity: You can use these fields to enter details about the room. However, as explained earlier, you can include some or all of this information in the room name so users can see it.
4. When you're finished, click Save to create the room mailbox.

Once you've created your room mailbox, you can edit your room mailbox to update info about booking options, MailTips and mailbox delegation. Check out the Use the Classic Exchange admin center section below to change room mailbox properties.

## Use Exchange  PowerShell to create a room mailbox in Exchange OnPremise or Exchange Online

This example creates a room mailbox with the following configuration:

- The mailbox's name is ConfRoom1. This name will also be used to create the room's email address.
- The display name in the Classic Exchange admin center and the address book will be Conference Room 1.
- The Room switch specifies that this mailbox will be created as a room mailbox.

```powershell
New-Mailbox -Name ConfRoom1 -DisplayName "Conference Room 1" -Room
```

How do you know this worked?

```powershell
Get-Mailbox <Name> | Format-List Name,RecipientTypeDetails,PrimarySmtpAddress
```
