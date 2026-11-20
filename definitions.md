### HXA.io definitions

==- Organization
An organization is the container for a company's profile, users, subscriptions, licenses, and other HXA.io entities.

==- Organization user
An organization user belongs to an organization and can receive portal permissions through a role. See [User Setup](/setup/user-setup.md) and [Role Setup](/setup/role-setup.md).

==- Subscription
A subscription is a type of container to store the purchased licenses.

==- License
A license gives the permission to use a specific product or service.

==- Connector
A connector is needed to establish a connection between the HXA.io system and a Microsoft service like Microsoft Exchange Online or Microsoft Teams. For HXA.io Roombooking a connection to an on-premise Exchange is possible too.

==- HXA.io Local Connector
The portal's automatically created connector for using HXA.io as a calendar host. It is distinct from the optional direct EWS connection between an HXA Display and a local Exchange server. See [Calendar Setup](/setup/calendar-setup.md).

==- Resource
A resource is a type of container where all information and settings of room calendar and devices are stored in.

==- Calendar
A calendar holds the bookings associated with a resource. Depending on the connection model, it can be hosted by HXA.io or provided by a Microsoft room/resource mailbox.

==- Device
A device can be a roombooking display.

==- Event protocol
At the event protocol you can find error messages.
===

### Microsoft definitions

==- Microsoft Teams team
A collaboration group bringing together members, conversations, files, and tools. Teams contain channels for organizing work. See [Microsoft's overview of teams and channels](https://learn.microsoft.com/en-us/microsoftteams/teams-channels-overview).

==- Microsoft Teams channel
A section within a team for conversations and work around a topic or project. Microsoft distinguishes standard, private, and shared channels. See [Microsoft's channel overview](https://learn.microsoft.com/en-us/microsoftteams/teams-channels-overview).

==- Microsoft resources
Bookable assets represented by resource mailboxes, such as meeting rooms or equipment. Users can include these mailboxes in meeting requests to reserve the asset. See [Microsoft's resource-mailbox documentation](https://learn.microsoft.com/en-us/exchange/recipients-in-exchange-online/manage-resource-mailboxes).

==- Microsoft resource mailbox
There are two types of resource mailboxes:
- Room mailboxes: location specific resources such as conference rooms, auditoriums, etc. 
- Equipment mailboxes: not location specific resources such as beamers, cars, etc.

==- Microsoft equipment mailbox
A resource mailbox for an asset that is not tied to a fixed room, such as a projector or company car. See [Microsoft's resource-mailbox documentation](https://learn.microsoft.com/en-us/exchange/recipients-in-exchange-online/manage-resource-mailboxes).

==- Microsoft workspace mailbox
An Exchange Online mailbox with the Workspace type, used for shared-workspace booking scenarios such as desk pools. Workspace is a cloud-only mailbox type. See [Set-Mailbox: Type](https://learn.microsoft.com/en-us/powershell/module/exchangepowershell/set-mailbox#-type) and [Microsoft Places desk-pool configuration](https://learn.microsoft.com/en-us/microsoft-365/places/configure-desk-booking).

===
