---
title: Grant permission for service account- Microsoft Exchange - HXA.io DOCS
label: Grant permission for service account
icon: paste
order: 99
---
# Grant permission for service account

When a resource mailbox is created in Microsoft Exchange a login disabled Active Directory user object will be made for this new resource mailbox. It is important, to hold this object disabled regarding the Microsoft licensing requirements. So the only way to access this kind of Mailboxes via an interface like HXA.io is to create a new logon allowed Active Directory user object that gets full permissions on the created resource mailbox. It's later called Service Account or delegate. If you use Microsoft Office 365 (Exchange Online) and you want to usa a HXA.io App Connector then you have not to create this service account but you can.

## Manage permission for service account

In Exchange Server, you can use the Exchange admin center (EAC) or the Exchange Management Shell to assign permissions for a mailbox. In our case we need t assign "Full access" (Allows the delegate to open the mailbox, and view, add and remove the contents of the mailbox. Doesn't allow the delegate to send messages from the mailbox. If you assign the Full Access permission to a mailbox that's hidden from address lists, the delegate won't be able to open the mailbox. By default, arbitration and discovery mailboxes are hidden from address lists.)

### Use the EAC to assign permissions to resource mailbox

1. In the EAC, click Recipients in the feature pane. Depending on the type of mailbox that you want to assign permissions for, click on one of the following tabs:
  - Resources: Room or equipment mailboxes.

2. In the list of mailboxes, select the mailbox that you want to assign permissions for, and then click Edit.
3. On the mailbox properties page that opens, click Mailbox delegation and configure one or more of the following permissions.
   - Full Access: The delegate can open the mailbox and do anything except send messages.

        To assign permissions to delegates, click Add Add icon. under the appropriate permission. A dialog box appears that lists the users or groups that can have the permission assigned to them. Select the user or group from the list, and then click Add. Repeat this process as many times as necessary. You can also search for users or groups in the search box by typing all or part of the name, and then clicking Search Search icon. When you're finished selecting delegates, click OK. 
   
        To remove a permission from a delegate, select the delegate in the list under the appropriate permission, and then click Remove Remove icon.

4. When you're finished, click Save.

### Source of information

[!badge variant="info" Badgtarget="blank" text="Manage permissions for recipients"](https://docs.microsoft.com/en-us/exchange/recipients/mailbox-permissions?view=exchserver-2019)