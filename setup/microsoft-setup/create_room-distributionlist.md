---
title: Create room distribution list - Microsoft Exchange - HXA.io DOCS
label: Create room distribution list
icon: paste
order: 99
---
# Create room distribution list

To summarize rooms and workspaces into groups you have to create a distribution group from type -RoomList via Exchange PowerShell. Room lists are specially marked distribution groups that you can use the same way you use distribution groups.

## Exchange OnPremise and Exchange Online

### Use Exchange PowerShell to create a room list

This example creates a room list for building 32.
```powershell
New-DistributionGroup -Name "Building 32 Conference Rooms" -OrganizationalUnit "contoso.com/rooms" -RoomList
```

### Use Exchange PowerShell to add a room to a room list

This example adds confroom3223 to the building 32 room list.
```powershell
Add-DistributionGroupMember -Identity "Building 32 Conference Rooms" -Member confroom3223@contoso.com
```

### Use Exchange PowerShell to convert a distribution group to a room list

You may already have created distribution groups in the past that contain your conference rooms. You don't need to recreate them; we can convert them quickly into a room list.

This example converts the distribution group, building 34 conference rooms, to a room list.
```powershell
Set-DistributionGroup -Identity "Building 34 Conference Rooms" -RoomList
```

### Source of Information

[!badge variant="info" Badgtarget="blank" text="Create a room list"](https://docs.microsoft.com/en-us/exchange/recipients-in-exchange-online/manage-resource-mailboxes#create-a-room-list)