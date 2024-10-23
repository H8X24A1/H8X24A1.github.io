---
title: Sparo App user documentation
label: HXA Sparo
icon: rocket
order: 90
---
# Overview 
**HXA Sparo** is an application designed to integrate seamlessly with Microsoft 365, allowing organizations to manage and book resources efficiently. It retrieves and displays resources set up by the organization, enabling users to quickly or schedule bookings, invite team members, and interact with **HXA Portal**.

HXA Sparo offers a variety of features, including resource management, floor plan mapping, and integration with organizational directories like Microsoft Active Directory. The application’s authentication process is handled through Microsoft 365 credentials, providing a secure and streamlined login experience.

## Key Features:
- **Quick and Scheduled Booking**: Instantly book available resources or schedule them for future use. You can either make a quick booking from the app’s interface or schedule a reservation for a later time.
- **Resource Management**: Fetch, book, and manage organizational resources such as meeting rooms, equipment, and workspaces.
- **Floor Plan Integration**: Link resources to specific areas on a floor plan and visually monitor their availability through a color-coded map.
- **Quick Bookings via QR Code**: Book resources quickly by scanning a QR code placed at the physical location.
- **Emergency Teams**: Access and contact your organization’s emergency response teams, viewing their availability and current location within the building.
- **Multi-language Support**: Switch between German and English interfaces for ease of use.
## Prerequisites
To use **HXA Sparo**, you need to:
- Purchase a license for **HXA Portal**.
- Have valid Microsoft 365 credentials for authentication.

Once the license is activated, users can log into **HXA Sparo** via the Microsoft 365 gateway using their organization's credentials.

## Integration with HXA Portal
**HXA Sparo** is deeply integrated with the **HXA Portal**, where administrators can manage resources and link them to floor plans. Resources such as meeting rooms, equipment, or areas on the floor map are linked to calendars, and their availability status is synced in real-time between the portal and **HXA Sparo**.

Administrators can:
- **Assign Calendars**: Link specific resource calendars to locations on the floor plan.
- **Manage Emergency Teams**: Import teams from Active Directory or manually create them in the **HXA Portal**.

## Security and Authentication
Authentication in **HXA Sparo** is handled via **Microsoft 365**, ensuring secure access to organizational resources. Users log in with their Microsoft 365 credentials through a gateway that grants access based on the organization's license.

## Conclusion
**HXA Sparo** is a powerful tool for managing organizational resources, floor plans, and emergency contact teams, all while integrating seamlessly with Microsoft 365 and the **HXA Portal**. Its intuitive interface and efficient booking system make it an essential app for companies looking to streamline their resource management and meeting planning processes.

# Download

## Get Sparo App

[![](/images/sparo/playstore256x80.png)](https://play.google.com/store/apps/details?id=com.hxa.sparo)

- [x] Download and install the HXA Room Booking App via <br><br>

[!ref target="blank" text="Google Play"](https://play.google.com/store/apps/details?id=com.hxa.sparo)  [!ref target="blank" text="Apple App Store"](https://apps.apple.com/de/app/hxa-sparo/id1672352267)

[![](/images/sparo/hxa.io_sparo_app_on_google_play.png)](https://play.google.com/store/apps/details?id=com.hxa.sparo)

# Login
## Prerequisites
To use **HXA Sparo**, you need to:
- Purchase a license for **HXA Portal**.
- Have valid Microsoft 365 credentials for authentication.

Once the license is activated, users can log into **HXA Sparo** via the Microsoft 365 gateway using their organization's credentials.


## Start up and login

- [x] Start the HXA Sparo App on your Android or iOS device

<img src="/images/sparo/hxa.io_sparo_sign_in.png" width="200">

<br><br>

- [x] Choose your language

<img src="/images/sparo/hxa.io_sparo_choose_language.png" width="200">

<br><br>

- [x] Login with your Microsoft 365 Company- or School account.

<img src="/images/sparo/hxa.io_sparo_ms365_login.png" width="200">

<br><br>

# Favorites

The **Favorites Tab** displays a list of resources that users have marked as favorites. These are often the most frequently used resources for quick access.


<img src="/images/sparo/favorites.jpeg" width="200">

# Available resources
This tab shows all resources available within the organization, alongside their current status:
- **Available**
- **Busy**
- **Pending**

Now you get shown a list of all current available rooms and workspaces of your company.

<img src="/images/sparo/availableresources.jpeg" width="200">

+++ Quick Booking and Scheduled Bookings
Instantly book available resources or schedule them for future use. You can either make a quick booking from the app’s interface or schedule a reservation for a later time.

You can see the capacity of each resource and by touching the booking button, you can quickly book the resource for immediate use. Simply choose the planned duration, and the resource is booked.

For scheduled bookings, users must use the fine filter to select specific times . to ensure the availability of the resource during the desired time. This helps refine search results for better scheduling accuracy.

<img src="/images/sparo/quickbooking.jpeg" width="200">
<br></br>
<img src="/images/sparo/scheduledbooking.jpeg" width="200">

# Filter

- **Filter by Time/Location**: Users can search for resources available at specific times or in particular locations.
If you want to book a resource for an appointment in the future, choose the filter option. There you can set a time frame to show all available resources in this time frame to book your meeting room or workspace.

<img src="/images/sparo/filter.jpeg" width="200">

<br></br>
<img src="/images/sparo/locationfilter.jpeg" width="200">

# Series Booking

The **Series Booking** feature in **HXA Sparo** allows users to create recurring reservations for meeting rooms or workspaces, similar to Microsoft Teams or Outlook. Users can schedule recurring bookings based on different intervals, and the system will handle each occurrence individually, allowing for granular control over edits or deletions.

### How to Create a Series Booking
To create a recurring (series) booking:
 Define the recurrence pattern:
   - **Daily**: Book the resource every day at the specified time.
   - **Weekly**: Book the resource on specific days of the week.
   - **Workdays**: Book the resource only on workdays (Monday through Friday).
   - **Monthly**: Book the resource on a particular day of each month.


The system will automatically create individual bookings for each occurrence, and you can view the full series in the **Bookings and Invitations Tab** under **My Bookings**.

### Managing a Series Booking
Once a series booking has been created, users can manage it as follows:

#### 1. Edit a Series
- Navigate to **My Bookings** in the **Bookings and Invitations** tab.
- Select the series booking you wish to modify.
- You will be prompted to choose:
  - **Edit Entire Series**: Apply changes to all occurrences (e.g., rescheduling the meeting time for every instance).
  - **Edit Single Occurrence**: Modify only one specific occurrence in the series (e.g., change the time for just one day).

#### 2. Delete a Series
- Navigate to the **Bookings and Invitations** tab and locate the series booking.
- You will be prompted to choose:
  - **Delete Entire Series**: Cancel all future occurrences of the booking.
  - **Delete Single Occurrence**: Cancel only one specific occurrence without affecting the rest of the series.


<img src="/images/sparo/seriesmeeting.jpeg" width="200">

# Scan QR Code

This tab allows users to book rooms by scanning QR codes placed in the physical locations. The app requires camera access for this functionality.

<img src="/images/sparo/qrscan.jpeg" width="200">

+++ Side Menu Features
## Side Menu Features
### 1. My Profile
The **My Profile** section displays user details fetched from the Microsoft 365 backend. The following fields are read-only:
- Name
- Surname
- Email
- Company Name
- Department
- Position
- Phone Number
- License Information

<img src="/images/sparo/profile.jpeg" width="200">


### 2. Settings
The **Settings** section includes the following configurable options:
- **Language Switcher**: Toggle between German and English interfaces.
- **Personal Status**: Update personal availability status (Free, Working Elsewhere, Tentative, Busy, Out of Office). This status is reflected when others attempt to invite the user to meetings.
- **Working Time**: This read-only information is pulled from the user's Microsoft 365 profile and reflects their work hours.
- **Date and Time Format**: Users can change the date and time format based on their location preferences, which will reflect in booking filters and other scheduling details.

<img src="/images/sparo/settings.jpeg" width="200">


### 3. About the Application
This section provides the **Terms of Use** and **Privacy Policy**, as set by NetTask.de, the provider of **HXA Sparo**.

<img src="/images/sparo/about.jpeg" width="200">


### 4. Report a Problem/Suggest Ideas
Users can report issues or submit suggestions directly from the application through this feature.

<img src="/images/sparo/support.jpeg" width="200">


### 5. Emergency Teams
The **Emergency Teams** feature displays a list of emergency contacts within the organization. Users can see the availability and location of team members (i.e., which room/resource they are currently in) and contact them by clicking on a phone icon next to their names.

<img src="/images/sparo/emergencyteam.jpeg" width="200">


#### Details:
- The list of emergency teams is imported from **Active Directory** or created manually in the **HXA Portal** by administrators.
- **HXA Sparo** simply renders these teams, while the portal manages their creation and import.

