# User Setup

Open **Account > Users** in the [HXA.io Portal](https://portal.hxa.io). **Users**, **Roles**, and **Groups** are separate pages in the Account menu.

## Find a user

Use **Search**, **Filter**, and **Columns option** to locate a profile. The user table includes:

- First name, Last name, and Email.
- Entra object ID and Entra ID information.
- Transponder-ID, marked **BETA**.
- Role, License Number, Status, and Last login To Portal.

## Create or import users

**Create user** opens a menu with two options:

| Option | Purpose |
| --- | --- |
| Create user | Open the portal's user-creation flow |
| Import Azure AD User | Import users from Microsoft Entra ID; the menu retains the Azure AD name |

For directory import, configure the Microsoft Entra ID connector first. Open **Create user > Import Azure AD User**, then select the users to import in the import workflow.

The overview also provides **Sync all users** and **Sync selected users**. Select the intended profiles before using synchronization for selected users. Review the result in the user list; importing or synchronizing users is separate from assigning their HXA licenses.

## Edit a user

Open the user's **Options** menu and choose **Edit user**.

| Section | Fields |
| --- | --- |
| BASIC INFO | First name, Last name, Department |
| CONTACT | Email, Mobile Phone, Business Phone |
| PREFERENCES & ACCESS | Language, PIN |
| VEHICLE & IDENTIFICATION | Vehicle Registration Plate, Transponder-ID [BETA] |
| PERMISSIONS | Role selection and user-license selection |

The PIN field displays an **8–16 digit** input hint. Availability of individual fields can vary; for example, contact fields can be read-only. Use **Save and Update** to save intended changes, then reopen the profile to check them.

For HXA Sparo, assign the license to the user in this form. See [License Assignment](/license/assign-license.md).

## Roles and primary contact

Manage role permissions under **Account > Roles**; see [Role Setup](/setup/role-setup.md).

The user Options menu also contains **Reset password**, **Delete User**, and **Set as a Primary contact**. These are separate actions from editing profile details. For the organization's primary contact, see [Organization Settings](/setup/organization-settings.md).

## Groups

Open **Account > Groups** for **Group Management**. The table shows **ID**, **Name**, **Type**, and **Entra ID**, with Search, Filter, and Columns option.

**Create Group** offers **Create Group** and **Import Azure AD Group**. Groups can also be selected in the organization's First Aid configuration; see [Emergency and safety settings](/setup/organization-settings.md#emergency-and-safety-settings).
