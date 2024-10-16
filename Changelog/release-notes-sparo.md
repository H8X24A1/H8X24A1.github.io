---
titile: HXA.io DOCS - HXA Sparo
label: HXA Sparo
icon: paste
order: 1100
---

## v3.2.1
Release date: 2024-10-15

+++ New :icon-shield-check:
- [x] Redesigned Maps, My Bookings, and Invitations.
- [x] Filters by location and categories.
- [x] Info box on Maps page for resource details.
- [x] Grid view for resources on all devices.
- [x] Error alerts for booking issues.

+++ Improved :icon-thumbsup:
- [x] Map preview shows resource availability/status.
- [x] Faster loading for My Bookings.
- [x] Declined bookings are now visible.
- [x] Updated Sync button design.
- [x] Tooltips for long names/locations.

+++ Fixed :icon-bug:
- [x] Sync box triggers correctly.

+++

## v3.0.0
Release date: 2024-09-25

+++ New :icon-shield-check:
- [x] Introducing the new "First Aid Helpers" feature within Organizations.
- [x] Upon first login, users are now presented with a series of onboarding introductory slides.


+++ Improved :icon-thumbsup:
- [x] Redesigned "Available Resources" and "Favorites" pages, providing a more engaging user experience.
- [x] Improved sync message layout for better visibility.


+++ Fixed :icon-bug:
- [x] Fixes in the application layout.
- [x] Fixes in the time format settings.

+++

## v2.1.1
Release date: 2024-09-20

+++ Improved :icon-thumbsup:
- [x] General improvements
- [x] Improvement of the rounding of a booking duration to 5-minute intervals.


+++ Fixed :icon-bug:
- [x] Fixed layout issues in the favorite maps area.
- [x] Fixed an issue when inviting external users.

+++

## v2.1.0
Release date: 2024-09-10

+++ Improved :icon-thumbsup:
- [x] Reduced the waiting time for the map page to load.
- [x] Added a feature that allows users to manually refresh available resources and favorites by scrolling down, ensuring real-time syncing .
- [x] Implemented caching for the "My Booking" page to enhance user experience and minimize the loading time for the booking list.


+++ Fixed :icon-bug:
- [x] Centered the filter description window after filter selection.


+++

## v2.0.0
Release date: 2024-08-26

+++ Improved :icon-thumbsup:
- [x] Implementation of advanced caching for available and favorite resources.
- [x] Added user notification update when pressing "Book now."
- [x] Introduced an option in the setting page to select date and time formats based on regional settings.


+++ Fixed :icon-bug:
- [x] Resolved layout and functionality issues caused by updated dependencies.

+++
## v1.8.2
Release date: 2024-08-12

+++ Improved :icon-thumbsup:

- [x] Optimized our code for faster navigation to "My Bookings" after booking an event.
- [x] Updated map shapes to support new designs.
- [x] Disabled start date edits for quick booking events on the "Edit" page.
- [x] Improve login/logout loading animation.


+++ Fixed :icon-bug:
- [x] Fixed infinite loading when quitting and resuming the app.
- [x] Aligned "Repeat" event icons and response options on "My Bookings" and "Invitations" pages.

+++
## v1.8.1
Release date: 2024-07-22

+++ Improved :icon-thumbsup:

- [x] Fetch the users' working hours from Microsoft and display it on the settings page.
- [x] Changed the shape of pictures of rooms and workspaces to rectangle with rounded corners.
- [x] A confirmation was added when a user wants to remove a resource from favorites.
- [x] Disabled the "until the end of the day" in event booking  if its a series booking. 


+++ Fixed :icon-bug:
- [x] The recurrence end date in series booking is now displayed correctly on iOS devices.
- [x] The layout of the favorite map has been adjusted for better usability.


+++
## v1.8.0
Release date: 2024-07-02

+++ Improved :icon-thumbsup:

- [x] We redesigned the layout in the Response Status section on the My Bookings - Invitation page to improve readability and display of detailed invitation information.
- [x] We reduced the App Log-in waiting time.
- [x] Users are now able to easily move the setting button up and down on the map page.


+++ Fixed :icon-bug:
- [x] Resolved the problem of editing an event even if it is booked till the end of the day.
- [x] The long-time waiting issue when the user quits and resumes to app is now resolved.
- [x] End Date in the recurrence filter is now showing on iOS devices.


+++

## v1.7.1
Release date: 2024-06-18

+++ Improved :icon-thumbsup:
- [x] Added another response “Tentatively ” option in the invitation page so that users can respond with it.
- [x] Users can now see notifications on "List of my bookings" tab to noitify that they have been invited to a meeting.
- [x] The images of the resources appears faster than before.

+++ Fixed :icon-bug:
- [x] Enhance the "Book Now" functions, So that the app performance would be faster.
- [x] Fix a bug in the availability resources on floor maps.

+++

## v1.7.0
Release date: 2024-06-11

+++ Improved :icon-thumbsup:
- [x] Added an Update button on the Map Page to refresh the "Floor Plan"     when Users will stay longer on this page.
- [x] Users can set a standard status "Show As" from the settings page to use this on the booking page.
- [x] Users can mark maps as favorites to review them anytime without filtering the map list.
- [x] Added an icon to indicate series events in the List of booking page.
- [x] Refactored all toast notifications into a toast service to improve loading performance.

+++ Fixed :icon-bug:
- [x] Fixed the wrong toast that appears in the floormap when email address is not correct.
- [x] Disabled the ability to change event time on the edit page if the "Till End of Day" toggle is on.
- [x] Fixed the highlighted slider issue when multiple sliders are available in the scheduled booking page.

+++


## v1.6.0
Release date: 2024-05-29

+++ Improved :icon-thumbsup:
- [x] The Accept/Decline icons in "My Bookings" have been repositioned for better usability.
- [x] Dynamic value updates are now available via the time slider when scheduling bookings.
- [x] The zoom function in maps has been made smoother for a better user experience.
- [x] Workspaces with a capacity of 1 now have their own default icon for easier identification.

+++ Fixed :icon-bug:
- [x] We handle an issue where the wrong Addresses of Resources can lead problems to show the map.
- [x] Problems encountered when booking resources have been fixed.
- [x] The maximum capacity of resources is now correctly displayed in the map view.
- [x] The organizer's status is now shown in the first position in the participant list for better visibility.
- [x] The error that occurred when deleting maps has been fixed.
+++

## v1.5.0
Release date: 2024-04-30

+++ Improved :icon-thumbsup:
- [x] Added a "My Status" option to the quick booking and scheduled booking to display the user status.
- [x] Enabled room booking directly through the map view page.
- [x] The user can now delete an event by swiping to the left.
- [x] You can now book an event by tapping on its name, and it will direct the user to the details page.
- [x] The map page will now be refreshed when the user navigates to another page and returns to the map page.

+++ Fixed :icon-bug:
- [x]  Resolved the white page issue that appears when resuming the app on the booking overview page.
- [x]  Addressed the bug that occurs when loading multiple maps.
- [x]  Reduced loading time in the booking overview.
- [x]  Fixed the bug in floor maps when applying filters on the floor label value.
+++

## v1.4.4
Release date: 2024-04-12

+++ Improved :icon-thumbsup:
- [x] Users can now add a title to events if they are booked via QR-code.
- [x] Enhanced the naming conventions for lists on the 'My Bookings' page.
- [x] Improved the messages that appear to the users after registration.

+++ Fixed :icon-bug:
- [x] Corrected translation errors in the feedback page between German and English languages.
- [x] Resolved issues with the event subject area on some booking pages.
+++

## v1.4.3
Release date: 2024-03-26

+++ Improved :icon-thumbsup:
- [x] Enhanced clarity for users encountering an error while quick booking.
- [x] Refined layout for both Quick Booking and Scheduled Booking for enhanced usability.
- [x] Enhanced design of the QR scan view for a more user-friendly experience.

+++ Fixed :icon-bug:
- [x] Rectified map display to ensure it appears at the minimum required size upon launch.
- [x] Added the organizer display to the "My Bookings" page in the "Invitations" tab for better clarity.
- [x] Redesigned components in the registration page to fit the layout.
+++

## v1.4.2
Release date: 2024-03-19
+++ Improved :icon-thumbsup:
- [x] My Booking Section: We have changed the tabs' naming to fit all content criteria and make it easier for the user to differentiate between bookings and invitations.


+++ Fixed :icon-bug:
- [x] QR scan  Fix: Fixed the QR scan page to enhance the quality of this feature and make it easier for users to scan via the application.
- [x] Questions and Feedback Fix:  Enhance the feedback questions to be able to deliver our point of view to the users, get accurate feedback, and act according to it.
+++

## v1.4.1
Release date: 2024-03-07
+++ New :icon-shield-check:
- [x] We implement a functionality to zoo maps in Mobile and Web Version
- [x] We added a new function that will allow to set a duration inside the Quick Booking so that the End-Time is automatically calculated

+++ Improved :icon-thumbsup:
- [x] We have made some general design improvements
- [x] We have done some small design improvements so that the text will fit better to the button size

+++ Fixed :icon-bug:
- [x] Fixed a problem in suggestions and ideas form 
- [x] Fixed a problem in the bottom menu
+++

## v1.4.0
Release date: 2024-01-30

+++ Improved :icon-thumbsup:
- [x] Enhanced Loading Time: Experience a significant boost in app performance with our high-impact loading time optimization. Get faster access to all your workspace and room booking needs without the wait.
- [x] Calendar Functionality Improved: Say goodbye to the frustrating 'jumping calendar' issue. We've ironed out this bug, ensuring a smoother, more reliable scheduling experience. Now, booking your workspace or meeting room is more seamless than ever.
- [x] User Interface Enhancements: Dive into a more intuitive and user-friendly app environment. Our latest UI fixes and improvements make navigating through the app more effortless and enjoyable, enhancing your overall booking experience.
+++

## v1.3.0
Release date: 2023-10-02

+++ New :icon-shield-check:
- [x] All-Day Booking - Users can now book for the entire day, offering more flexibility in scheduling.

+++ Improved :icon-thumbsup:
- [x] Navigation Bar Highlighting - The active icon on the navigation bar is now more prominently highlighted, making it easier to identify the current page or section.
- [x] Layout Update for Editing and Booking Pages - We've revamped the layout on the editing and booking pages. Additionally, users can now select an end date for their bookings.
- [x] Loading Time Optimization - Significant improvements have been made to reduce loading times across the platform, ensuring a faster and more responsive user experience.
- [x] Favorites Page Capacity Display - On the favorites page, we've enhanced the display of capacity. Users can now see both the booked and possible capacity, providing a clearer overview of availability.
- [x] Several other small improvements

+++ Fixed :icon-bug:
- [x] Filter Persistence Issue - Resolved an issue where the filter would retain filter settings as users navigated across different pages in the app. The filter now resets appropriately, ensuring accurate results based on user preferences.
+++

## v1.2.3
Release date: 2023-10-25

+++ Fixed :icon-bug:
- [x] Bug fix Correction of an error when displaying the time period within the schedule booking which is available via the favorites.
+++

## v1.2.2
Release date: 2023-1020

+++ New :icon-shield-check:
- [x] Favorite Page Integration: We've integrated the Favorite page into the Homepage. This not only allows for a more personalized experience but also ensures faster loading times.
- [x] Scheduled Booking: Users can now schedule bookings directly from the Favorite page. We've made it even more convenient by displaying available time slots based on the selected resource's calendar.
- [x] Enhanced search
- [x] Resource Management

+++ Improved :icon-thumbsup:
- [x] iPad Design Update
- [x] Performance Enhancements

+++Fixed :icon-bug:
- [x] Filter Persistence Issue - Resolved an issue where the filter would retain filter settings as users navigated across different pages in the app. The filter now resets appropriately, ensuring accurate results based on user preferences.
+++

## v1.1.0
Release date: 2023-09-19

+++ New:icon-shield-check:
- [x] Add Resources to your favorite list and book directly from the list of your favorites.
- [x] Schedule whole day bookings.

+++Fixed :icon-bug:
- [x] General performance improvements.
+++

## v1.0
Release date: 2023-07-12

+++ New :icon-shield-check:
- [x] Book your ideal workspace in Microsoft 365 with the HXA Sparo App. Fast bookings, diverse options, and seamless integration await you!
- [x] Find your perfect workspace in Microsoft 365 or Exchange Online and soon in Exchange OnPremise or Exchange Hybrid Deployments.
- [x] Looking for a workplace that suits your needs? Look no further! With our Microsoft 365-powered app, you can easily book seats and conference rooms with just a few taps on your mobile device.
- [x] Whether you need a quiet place to focus, a comfortable place to brainstorm with your team or a state-of-the-art conference room, our HXA Sparo app covers you.

Key features of our HXA Sparo app include:
- [x] + Fast and easy booking process.
- [x] + Variety of workspaces and meeting rooms to choose from.
- [x] + Full integration with your Microsoft 365 account.

Finding the perfect workplace has never been easier with our HXA Sparo app. Just open the app, search for available seats, and book your seat within minutes.

Ready to take your productivity to the next level? 
Download our HXA Sparo app today and start enjoying the perfect modern or hybrid workspace experience in your company.

+++
